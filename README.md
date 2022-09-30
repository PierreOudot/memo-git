#**Memo de commandes git**

##**initialisation de la source local et lien avec le repo distant**
*git init* : initialise le fichier git.init dans le dossier local de travail
*git add remote origin user@http* : lier init et user distant

##**modifications de fichiers**
*git commit -option "nom_commit"* : sauvegarder les modif à un instant t
*git push* : envoyer les commits sur le repo distant

##**gestion des branches**
*git branch"nom_branche"*: créer une nouvelle branche
*git checkout nom_branche*: changer de branche (deplace HEAD sur dernier commit de ladite branche).
*git merge nom_branche*:fusionne la branche ciblée avec la branche active.
*git rebase nom_branche_cible*+
n peut utiliser seulement les 4 premiers car de l'id applique un historique
*git rebase nom_branche_source*: ajoute la copie d'1 ensemble de commits de la branche cible dans la branche source
##**gestion des commit**
*git checkout id_commit*: deplace la HEAD sur le commit ciblé
###**references relatives**
permet de reoganiser les branches
*id/HEAD^*: remonte d'1 commit depuios le commit ciblé/HEAD
*~nombre*: remonte de nombre depuis le commit/head
###**annuler les modifications**
*git reset commitID/HEAD+operateur ref relative*: revenir x commit en arriere sur repo local
*git revert commitID/HEAD+operateur ref relative*: revenir x commit et modifier le repo distant.ajoute un nouveau commit (commit') contenant l'historique des modif###**annuler les modifications**
*git reset commitID/HEAD+operateur ref relative*: revenir x commit en arriere sur repo local
*git revert commitID/HEAD+operateur ref relative*: revenir x commit et modifier le repo distant.ajoute un nouveau commit (commit') contenant l'historique des modif.marche sur commit déja push.

