---
title: "Multilingue"
date: 2021-11-18T21:15:54+01:00
weight: 7
draft: false
---
***
Hugo vous permet de paramétrer le multilangue pour adapter les pages dans la langue souhaitée.

Pour ce faire, nous modifions d'abord le fichier de configuration en paramétrant les langues.Dans le cas de la pratique, j'ajoute l'anglais, le français et l'espagnol.

    [Languages]
        [Languages.es]
            title = "Ejemplo para el uso de idiomas"
            weight = 1
            languageName = "Español"
        [Languages.en]
            title = "Example use language"
            weight = 2
            languageName = "English"
        [Languages.fr]
            title = "Exemple d'utilisation des langues"
            weight = 3
            languageName = "Français"
Dans ce cas, nous allons établir différents répertoires pour établir l'emplacement des fichiers. Un menu devrait apparaître pour afficher les différentes options de menu.

Nous pouvons maintenant établir une langue par défaut également avec des variables dans le fichier config.toml

    defaultContentLanguage = 'fr'

Dans le cas d'learn, la page qui nous montre, s'il n'y a pas de contenu dans le dossier de contenu, c'est le contenu du fichier index.html. Si nous le saisissons, et voyons ainsi comment utiliser la structure de contrôle dans un modèle , nous pouvons clairement voir où il se trouve Localisez la traduction, puisque par défaut, ce modèle est préparé pour l'anglais et le français. Ajoutons l'espagnol. Pour ce faire, observez et utilisez la structure de contrôle if - else if - end les structures de contrôle de syntaxe.

Des modifications doivent également être apportées en copiant les fichiers dans le dossier de mise en page

    {{if eq .Site.Language.Lang "fr"}}
       <h1>Personaliser la page d'accueil</h1>
   
    {{else if eq .Site.Language.Lang "es" }}
       <h1>Personaliza tu página principal</h1>
   
    {{else if eq .Site.Language.Lang "en"}}
           <h1>Customize your own home page</h1>
    {{end}}




