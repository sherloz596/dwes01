---
title: "Teneur"
date: 2021-11-17T09:48:43+01:00
weight: 4
draft: false
---
***
Pour créer un nouveau contenu, nous allons générer des pages de texte au format Markdown.
Nous examinons comment nous utilisons différents répertoires pour créer notre organisation de notre contenu.

Chaque répertoire correspondra à une section.

Dans chaque section, il peut y avoir un fichier _index.md dont le contenu sera affiché lorsque nous sélectionnerons le répertoire spécifique.

Commande pour créer des fichiers de contenu et/ou des sections :

    hugo new [section]/déposer.md

Dans le cas particulier du modèle d'apprentissage, les pages sont classées en deux types, celles qui sont en tête d'un sujet ou d'une section (_index.md) et celles qui ont leur contenu.

Pour créer une page qui est un en-tête de chapitre (nous créons la section théorie et le fichier _index.md) :

    hugo new chapter --kind theorie/_index.md


Pour créer un fichier dans la section théorie

    hugo new chapter --kind theorie/tema1.md

Lorsque nous générons du contenu, les fichiers créés nous voyons que dans l'en-tête ou les premières lignes ils peuvent avoir des méta-informations. Cette information passe entre trois lignes et constitue ce qu'on appelle le **front matter** de la page Dans cette section, nous donnerons des valeurs aux variables qui pourront être utilisées ultérieurement.

Parmi les différentes valeurs, nous souhaitons en voir certaines qui sont généralement dans les archtypes et apparaissent généralement par défaut :

+ **titre** sera le titre auquel cette page devra être référencée dans les différents menus
+ **poids** est l'un des moyens d'ordonner les pages et les sections.
+ **brouillon** Indique si la page est un vrai brouillon ou non. S'il s'agit d'un brouillon, vous nous verrez.
+ **description** C'est une description qui apparaîtra sur la page principale ou l'index de cette section. Il apparaîtra pour chaque page, sauf s'il est précisé que nous n'en voulons pas. Affichera.

