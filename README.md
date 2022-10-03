# **Memo de commandes git**

## **Creation de depot distant**

*git clone + lien repo distant*: copier le repo distant en local
```convention de nommage des branche: <nom_depot_distant>/<nom_branche>
```nom de repo distant est souvent origin

## **initialisation de la source local et lien avec le repo distant**

*git init* : initialise le fichier git.init dans le dossier local de travail
*git add remote origin user@http* : lier init et user distant

## **recuperation depuis le depot distant**

*git fetch*: recupère depuis un depot distant, mise à jour des bracnhes distante: recupère depuis un depot distant, mise à jour des bracnhes distantesomble le retard de la branche lcoale vs depot distant.

## **modifications de fichiers**

*git commit -option "nom_commit"* : sauvegarder les modif à un instant t
*git push* : envoyer les commits sur le repo distant

## **gestion des branches**

*git push --set-upstream origin nom branche* :connecter la branche locale à sa version distante
*git branch"nom_branche"*: créer une nouvelle branche

*git checkout nom_branche*: changer de branche (deplace HEAD sur dernier commit de ladite branche).

*git merge nom_branche*:fusionne la branche ciblée avec la branche active.

*git rebase nom_branche_cible*+

*git rebase nom_branche_source*: ajoute la copie d'1 ensemble de commits de la branche cible dans la branche source

## **gestion des commit**

*git checkout id_commit*: deplace la HEAD sur le commit ciblé. On peut utiliser seulement les 4 premiers car de l'id applique un historique

### **references relatives**

permet de reoganiser les branches

*id/HEAD^*: remonte d'1 commit depuios le commit ciblé/HEAD

*~nombre*: remonte de nombre depuis le commit/head

### **annuler les modifications**

*git reset commitID/HEAD+operateur ref relative*: revenir x commit en arriere sur repo local

*git revert commitID/HEAD+operateur ref relative*: revenir x commit et modifier le repo distant.ajoute un nouveau commit (commit') contenant l'historique des modif

### **annuler les modifications**

*git reset commitID/HEAD+operateur ref relative*: revenir x commit en arriere sur repo local

*git revert commitID/HEAD+operateur ref relative*: revenir x commit et modifier le repo distant.ajoute un nouveau commit (commit') contenant l'historique des modif.marche sur commit déja push.

*git restore + option+ fichier*: permet d'extraire et de copier un arbre de travail/index depuis une source.

*git restore --staged*: restore uniquement l'index.

### **Tagging**

permet de marquer un état comme important et de retrouver ces états via leurs étiquettes.

*git tag version*: si pas d'option -asm = étiquette légère, pas d'info stockées, juste le checksum du commit correspondant 

*git tag -a version -m"message": créer un tag annoté, = objet à part entière, contient toutes infos liées au commit et au créateur.

*git tag -d version-lw : supprimme l'étiquette correspondant à version, besoin d'être push pour être validé sur repo distant. utiliser la commande *git push origin version"* pour push le tag

### **gestion des issues**

le commit qui resoud une issue doit comporter commme message "resolve #id_issue". Après pull request et merge des branches, l'issue sera résolue.


