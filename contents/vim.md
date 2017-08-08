# Vi IMproved

Le plus tricky des éditeurs de texte modal !

---

## Overview

[Vim] est un **éditeur de texte** pour le terminal sous GNU/Linux. Directement inspiré
de **vi**, il possède une stabilité exemplaire, une quantité de fonctions très apprécié 
des développeurs (coloration syntaxique de 200 langages, complétion automatique, 
comparaison de fichiers, recherche évoluée) et est extensible par des scripts.

Certes très austère, c'est pourtant un outil véritablement très puissant pour ceux 
capables le dompter.


## Principe de base

Pour **créer ou modifier un fichier** avec vim utilisez la commande suivante :

```bash
vim my_file_path
```

Si le fichier n'existe pas il sera créé automatiquement.

!!! Note

    Et voilà, le fichier s'affiche et vous êtes dans le **mode commande**. Pour déplacer le curseur utilisez 
    les flèches ou les touche `H, J, K, L`. C'est dans ce mode que vous pouvez entrer des commandes 
    pour agir sur le texte. 
    
    Appuyez sur ` i ` pour accéder au **mode insertion** ou ` Échap ` pour en sortir.


## Commandes de base

Commandes | Action
------------ | -------------
` i ` | Passer dans le mode insertion
` A ` | Ajouter en fin de ligne
` 0 ou $ ` | Se déplacer en début ou fin de ligne
` :q ` | Quitter
` :q! ` | Quitter sans enregistrer
` :w ` | Enregistrer le fichier
` :wq ` | Enregistrer et quitter
` :x ` | Enregistrer (seulement en cas de modification) et quitter
` :set paste ` | Passer en mode "collage"


## Commandes d'édition

Commandes | Action
------------ | -------------
` u ` | Annuler la dernière opération
` <control>-r ` | Rétablir la dernière opération annulée
` . ` | Répéter la dernière opération d'édition
` yy ` | Copier la ligne (*4yy = 4 lignes*)
` dd ` | Couper la ligne (*4dd = 4 lignes*)
` d0 ou d$ ` | Supprimer le début ou la fin de la ligne
` p ` | Coller après (*P = insérer avant*)
` x ` | Effacer le caractère
` dw ` | Effacer le texte jusqu'à la fin du mot
` diw ` | Effacer le mot sous le curseur
` G ` | Sauter à la ligne (*7G pour la ligne n°7*), par défaut le curseur sute à la dernière ligne
` gg ` | Sauter à la première ligne


!!! Note

    Taper un nombre avant une commande vous permettra d'exécuter la commande plusieurs fois... 


## Recherche / Remplacement

Commandes | Action
------------ | -------------
` / ` | Rechercher du texte (*` ? ` pour remonter dans le fichier*)
` n ` | Rechercher l'occurence suivante
` N ` | Rechercher l'occurence précédente
` cw ` | Remplacer le texte jusqu'à la fin du mot
` ciw ` | Remplacer le mot
` C ` | Remplacer jusqu'en fin de ligne
` . ` | Répéter la dernière opération d'édition
` :s/ancien/nouveau/g ` | Rechercher et remplacer du texte à la ligne où se trouve le curseur
` :%s/ancien/nouveau/g ` | Rechercher et remplacer du texte
` :r file_name ` |  Insérer un fichier à la position du curseur


## Fenêtrage

Commandes | Action
------------ | -------------
` <control-w>-s ou :sp ` | Diviser horizontalement
` <control-w>-v ou :vsp ` | Diviser verticalement
` <control-w>-h/j/k/l ` | Passer à la fenêtre suivante
` <control-w>-w ` | Passer à la fenêtre suivante
` <control-w>-+ ` | Agrandit le viewport actuel
` <control-w>-- ` | Réduit  le viewport actuel
` <control-w>-= ` | Egalise à nouveau la taille des viewports.
` <control-w>-r ` | Echange la position des viewports (*` R ` pour le sens inverse*)
` <control-w>-n ` | Ouvrir un fichier vierge dans une nouvelle fenêtre
` <control-w>-q ` | Fermer la fenêtre

---

### Getting help

[Documentation Ubuntu][VimDoc]

[Documentation OpenClassrooms][VimOpenclassrooms]

[Vim]: http://www.vim.org/
[VimDoc]: https://doc.ubuntu-fr.org/vim
[VimOpenclassrooms]: https://openclassrooms.com/courses/reprenez-le-controle-a-l-aide-de-linux/vim-l-editeur-de-texte-du-programmeur
