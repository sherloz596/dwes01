---
title: "Multilanguage"
date: 2021-11-18T21:15:54+01:00
weight: 7
draft: false
---
***
Hugo allows you to set the multilanguage to adapt the pages in the desired language.

To do this, we first modify the configuration file by setting the languages. In the case of practice, I add English, French, and Spanish.

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

In this case we are going to establish different directories to establish the location of the files. A menu should appear to view the different menu options.

Now we can establish a default language also with variables in the config.toml file

    defaultContentLanguage = 'en'

In the case of learn, the page that shows us, if there is no content in the content folder, it is the content of the index.html file. If we enter it, and thus see how to use the control structure in a template, we can clearly see where it is Locate the translation, since by default, this template is prepared for English and French. Let's add Spanish. To do this, observe and use the control structure if - else if - end syntax control structures.

Modifications must also be made by copying the files into the layout folder

    {{if eq .Site.Language.Lang "fr"}}
       <h1>Personaliser la page d'accueil</h1>
   
    {{else if eq .Site.Language.Lang "es" }}
       <h1>Personaliza tu página principal</h1>
   
    {{else if eq .Site.Language.Lang "en"}}
           <h1>Customize your own home page</h1>
    {{end}}