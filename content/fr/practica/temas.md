---
title: "Les sujets"
date: 2021-11-16T20:26:52+01:00
weight: 3
draft: false
---
***
Nous avons différentes manières d'installer un modèle.

Tous doivent laisser dans le dossier des thèmes de notre projet un dossier avec le développement du modèle que nous allons télécharger depuis git

Les moyens d'obtenir ce dossier peuvent être :

1. Téléchargez le développement et décompressez-le dans le dossier
2. Clonez directement dans le dossier avec git clone
3. Clonez-le en tant que sous-module à partir du dossier du projet

J'ai utilisé la troisième voie. Pour ce faire à partir du répertoire du projet, j'ai d'abord créé un référentiel vide :

    git init

Après l'avoir cloné en tant que sous-module :

    git submodule add https://github.com/matcornic/hugo-theme-learn.git themes/learn

Enfin j'ai modifié le fichier de configuration config.toml indiquant l'emplacement du thème :

    theme = 'learn'


