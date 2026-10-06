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
```


### Question 3.7

Il ne voit plus aucune erreur dans le git status pour le README.md rien de manquant.

### Question 3.8

```
491491f (HEAD -> main) meow
e6842a6 Ajout du compte rendu (question 0 à 3.5)
5752504 Création du README
```

Il est préférable de faire de commit car c'est mieux d'avoir un historique plus clair.

### Question 4.1

Le git show montre les informations de tout le code source du fichier.

### Question 4.2

git restore permet de restaurer le fichier qui a été a la derniere version à jour dans GIT. On ne pourrait pas récupérer le fichier si il n'avait jamais été commité. (si il y avait qu'ne seule version)
### Question 4.3 

Le fichier n'a pas été supprimé du disque. Mais le fichier est dans une zone de l'ordinateur, il est dans le local mais pas dans GIT

### Question 4.4

les fichier qui ont disparu de la réponse de git status c'est test.txt brouillon.txt erreurs.log debug.log. ```*.log``` signifie que tout les fichier contenant cette extention vont être caché.

le fichier qui y apparait c'est le .gitignore, et faut le committer.

### Question 4.5 




### Question 5.2
les 2 fichiers qui ont été crée c'est la clé ssh privé et publique. la privé c'est celle qui n'a pas d'extention de fichier et la publique c'est la .pub

### Question 5.4

``` cpp
Hi clementboivin! You've successfully authenticated, but GitHub does not provide shell access.
```
La clé publique est une clé ouverte qui permet pour github de nous reconnaitre, on peut la donner car c'est un cadena ouvert y a pas de sécurité.

### Question 6.3

1. 

``` cpp

origin	git@github.com:clementboivin/tp01-git.git (fetch)
origin	git@github.com:clementboivin/tp01-git.git (push)
```

```cpp
Énumération des objets: 12, fait.
Décompte des objets: 100% (12/12), fait.
Compression par delta en utilisant jusqu'à 12 fils d'exécution
Compression des objets: 100% (10/10), fait.
Écriture des objets: 100% (12/12), 1.87 Kio | 319.00 Kio/s, fait.
Total 12 (delta 2), réutilisés 0 (delta 0), réutilisés du pack 0
remote: Resolving deltas: 100% (2/2), done.
```
2. L'historique n'est pas le même que celui de git log --oneline car il affiche pas les clé crypté. le fichier brouillon n'est pas la car il n'a pas été commiter

### Question 6.4 a

Il nous dit que le commit le plus récent est sur github avec origin/main

### Question 6.4 b

Il c'est passé que le dossier tp01 a été sauvagardé dans le origin/main qui est sur github.

l'auteur du dernier commit c'est l'utilisateur de github

### Question 6.5

```cpp

Répertoire de travail --( git add )--> Zone de préparation --( git commit )--> Dépôt local --( git push )--> GitHub
          ^                                                                                     |
          +--------------------------------------( git pull)------------------------------------+

```

### Question 7.1

le clone contient uniquement la derniere version des fichiers.
le fichier brouillon.txt n'est pas dans le clonne car il n'a jamais été commiter ni ajouter dans git.
Il n'y a pas eu besoin de faire un git init car c'etait déjà un fichier présent sur github.

### Question 7.2

