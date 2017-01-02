Mon rapport de stage
===========

Pour la validation du stage du fin d'année, l'Epita me demande un rapport de
fin d'étude et une soutenance. Ce dépôt représente les livrables demandés.

## What's here

* **rapport/**
    * Contient le rapport de stage au format Latex
    * Version pdf disponible mais pas forcément à jour
* **soutenance/**
    * Contient les slides qui seront utilisés lors de la
  soutenance de fin d'étude
* **abstract/**
    * Contient un résumé en anglais du rapport au format Latex
    * Version pdf disponible
* **ressources/** :
    * Contient les ressources utiles au développement du rapport
    * Un gantt fait sous [Omniplan][2]
  avec le planning du stage et la rédaction du rapport de stage

### Résumé

Quelques lignes sur le sujet du rapport ici

## Avancement

Livrable                    |   Avancement          |
------------                |   -------------       |
Rapport de stage            |   [..........]  1 %   |
Rapport anglais             |   [..........]  0 %   |
Présentation soutenance     |   [..........]  0 %   |

# Manuel d'installation

## Installation sous OSX

1. Installer [MacTex][1] via le site ou en ligne de commande via Homebrew
2. Étendre le PATH pour accéder aux nouvelles commandes
3. Lancer le makefile

```sh
$> brew cask install mactex
$> export PATH=$PATH:/Library/TeX/texbin
$> make
```

[1]: http://www.tug.org/mactex/
[2]: https://www.omnigroup.com/omniplan

## Utilisation

* Compile et ne garde que le pdf : `make`
* Compile et garde les fichiers intermédiaires : `make dev`
* Supprime tous les fichiers intermédiaires : `make clean`
* Pour lire le pdf : `make read`

## Tips

Si les modifications sont faites avec vim :

* Ne pas oublier d'activer le spell mode afin d'obtenir une correction
orthographique -> [vimrc#spellmode](https://github.com/mydoum/dotfiles/blob/master/vimrc#L91)
* Ajouter les dictionnaires français dans le dossier spell ->
  [vimfolder](https://github.com/mydoum/dotfiles/tree/master/vim/spell)

## Reminders

Sont utilisés :

* Latexmk   : Pour compiler
* Bibtex    : Pour la bibliographie
* Biblatex  : Pour les citations en footnote

* **config.tex**
    * Configure le style des chapitres, headers, footers
    * Configure lslisting pour embarquer du code
    * Propose la commande `\tail` pour annonce la fin du document
    * Propose la commande `\blankpage` pour sauter une page blanche
* **includes/bibliography.tex**
    * Contient toutes les citations bibliographiques
    * Utiliser `\autocite{element}`
* **includes/glossary.tex**
    * `\gls` pour utiliser un élément du glossaire ou d'abréviation
    * `\glspl`sa forme plurielle, mais doit être précisé lors de sa création
    * `\Gls` met une majuscule sur la première lettre
* **includes/acronyms.tex**
    * Acronymes
    * `\printglossaries` affiche le glossaire puis les acronymes
