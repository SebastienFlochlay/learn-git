## Les bases de Git

### Initialiser un dépot

Vous pouvez initialiser un dépot de deux manières. La première consiste à prendre un projet ou un répertoire 
existant et à l’importer dans Git. La seconde consiste à cloner un dépôt Git existant sur un autre serveur.

#### Initialisation d’un dépôt Git dans un répertoire existant
Si vous commencez à suivre un projet existant dans Git, vous n’avez qu’à vous positionner dans le répertoire 
du projet et saisir :

```bash
$ git init
```

Cela crée un nouveau sous-répertoire nommé ` .git ` qui contient tous les fichiers nécessaires au dépôt. 

### Cloner un dépôt existant

Si vous souhaitez obtenir une copie d’un dépôt Git existant, la commande dont vous avez besoin s’appelle ` git clone `. 
Il est important de bien comprendre qu'avec cette commande, Git reçoit une copie de quasiment toutes les données 
dont le serveur dispose. Toutes les versions de tous les fichiers pour l’historique du projet sont téléchargées 
quand vous lancez git clone.

```bash
$ git clone https://github.com/Kotlin/kotlin-koans.git
```

Ceci crée un répertoire nommé “kotlin-koans”, initialise un répertoire .git à l’intérieur, récupère toutes les données 
de ce dépôt, et extrait une copie de travail de la dernière version. Si vous souhaitez cloner le dépôt dans un 
répertoire nommé différemment, vous pouvez spécifier le nom dans une option supplémentaire de la ligne de commande :

```bash
$ git clone https://github.com/Kotlin/kotlin-koans.git my-kotlin-koans
```

Cette commande réalise la même chose que la précédente, mais le répertoire cible s’appelle my-kotlin-koans.


