# Git

Système de gestion de version décentralisé open source.

---

## Définition

### Gestionnaire de version

Un gestionnaire de version (VCS - Version Control System) est un système 
qui trace et enregistre l'évolution d'éléments au cours de vos développements.
Ce qui vous permet de revenir rapidement à une version antérieure d'un fichier, 
de ramener le projet complet à un état précédent, de visualiser les changements 
au cours du temps, de voir qui a modifié quelque chose qui pourrait causer un 
problème, qui a introduit un problème et quand, et plus encore. 
Utiliser un VCS signifie aussi généralement que si vous vous trompez ou que 
vous perdez des fichiers, vous pouvez facilement revenir à un état stable.


## Installation de Git

Pour l'installation de Git, vous trouverez tout le nécessaire sur le site [git-scm.com]. 
Choisissez votre plateforme et procédez à l'installation.

## Git et son Paramétrage

Maintenant que Git est installé, il est important de personnaliser votre environnement 
Git dés à présent. Git contient un outil nommé ` git config ` qui vous permet de configurer 
Git à votre convenance. Pour information, ces variables de configuration peuvent être 
stockées dans trois endroits différents :


* ` --system `

Le fichier ` /etc/gitconfig ` contient les valeurs pour tous les utilisateurs et tous les dépôts du système. 
Si vous passez l’option ` --system ` à git config, il lit et écrit ce fichier spécifiquement.

* ` --global `

Le fichier ` ~/.gitconfig ` est spécifique à votre utilisateur. Vous pouvez forcer Git à lire et écrire 
ce fichier en passant l’option ` --global `.

* ` --local `

Le fichier config dans le répertoire Git (c’est-à-dire ` .git/config ` ) du dépôt en cours d’utilisation est
spécifique au seul dépôt en cours. C'est le niveau par défaut lorsque vous utilisez la commande ` git config `,
mais vous pouvez bien sûr tout aussi bien utiliser l'option ` --local `.


!!! Note
    
    Chaque niveau surcharge le niveau précédent, donc les valeurs dans .git/config surchargent 
    celles de /etc/gitconfig.

#### Votre identité

La première chose à faire après l’installation de Git est de renseigner votre nom et votre adresse mail. 
C’est une information importante car toutes les validations dans Git utilisent cette information et elle est 
indélébile dans toutes les validations que vous pourrez réaliser :

```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

Si vous avez bien suivi Cette étape n’est nécessaire qu’une fois puisque vous passez l’option ` --global `. Si vous 
souhaitez surcharger ces valeurs avec un nom ou une adresse mail différents pour un projet spécifique, vous pouvez 
lancer ces commandes sans option ` --global ` lorsque vous êtes dans ce projet.

#### Votre éditeur de texte
À présent que votre identité est renseignée, vous pouvez configurer l’éditeur de texte qui sera utilisé quand Git 
vous demande de saisir un message. Par défaut, Git utilise l’éditeur configuré au niveau système, qui est 
généralement Vi ou Vim. Si vous souhaitez utiliser explicitement VIM vous pouvez entrer ce qui suit :

```bash
$ git config --global core.editor vim
```

Voici une liste récapitulant quelques exemples d'éditeur de texte :

Editeur | Commande
------------ | -------------
Atom | ` git config --global core.editor "atom --wait" `
emacs | ` git config --global core.editor "emacs" `
nano | ` git config --global core.editor "nano -w" `
vim | ` git config --global core.editor "vim" `
Sublime Text (Mac) | ` git config --global core.editor "subl -n -w" `
Sublime Text (Win, 32-bit install) | ` git config --global core.editor "'c:/program files (x86)/sublime text 3/sublimetext.exe' -w" `
Sublime Text (Win, 64-bit install) | ` git config --global core.editor "'c:/program files/sublime text 3/sublime_text.exe' -w" `
Textmate | ` git config --global core.editor "mate -w" `

#### Lister vos paramètres

Il est bien sûr possible de vérifier vos réglages en listant vos paramètres via la commande suivante **` git config --list `** :

```bash
$ git config --list
user.name=John Doe
user.email=johndoe@example.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
```

Vous pourrez observer certains paramètres apparaître plusieurs fois dans votre list, et c'est normal puisque Git liste 
les mêmes paramètres depuis plusieurs fichiers (/etc/gitconfig et ~/.gitconfig, par exemple). 
Il suffi de savoir que Git utilise la dernière valeur pour chaque paramètre.

En cas de doute, vous pourrez vérifier la véritable valeur d'un paramètre en spécifiant sont nom :

```bash
$ git config user.name
John Doe
```

## Obtenir de l’aide

En cas de souci sur une commande, vous pouvez toujours jeter un œil au manuel.

```bash
$ git help <commande>
$ git <commande> --help
$ man git-<commande>
```

[git-scm.com]: https://git-scm.com/downloads