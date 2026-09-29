# Compte rendu TP01 - Découverte de GIT


### Question 0 
La version de Git installé est 2.43.0

### Question 1 
https://github.com/clementboivin

### Question 2

```
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs 
filter-process
filter.lfs.required=true
filter.lfs.clean=git-lfs clean -- %f
user.name=clement-boivin
user.mail=clementboivin96@gmail.com
init.defaultbranch=main
core.editor=nano
```

l'option  --global signifie que ca va sortir en globalité de la config

### Question 3.1

git status répond : fatal: ni ceci ni aucun de ses répertoires parents (jusqu'au point de montage /) n'est un dépôt git
Arrêt à la limite du système de fichiers (GIT_DISCOVERY_ACROSS_FILESYSTEM n'est pas défini).

Parceque c'est pas encore un repertoire git

### Question 3.2 

git init a créer un dossier .git on le vois pas car c'est un fichier invisible

git status renvoie aucun commit n'est créer.

### Question 3.3 

git status a rangé README.MD dans le repertoire local mais pas dans le repertoire git car il n'est pas validé.

### Question 3.4

git status a changé de réponse car c'est un fichié validé par git il a été rajouté. (affiché en vert)

### Question 3.5

```cpp
commit 5752504a88acfa14a7ad44952761f69432f650af (HEAD -> main)
Author: clement-boivin <cboivin@d117-03.lab.rascol-info.org>
Date:   Tue Sep 29 16:35:10 2026 +0200



###