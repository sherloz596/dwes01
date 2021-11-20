---
title: "Multilenguaje"
date: 2021-11-18T21:15:54+01:00
weight: 7
draft: false
---
***
Hugo permite establecer el multilenguaje para adaptar las páginas en el lenguaje deseado.

Para ello, lo primero modificamos el fichero de configuración estableciendo los idiomas.En el caso de la práctica añado inglés, francés, y español.

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
En este caso vamos a establecer diferentes directorios para establecer la ubicación de los ficheros. Deberá de aparecer un menú para ver las diferentes opciones del menú.

Ahora podremos establecer un idioma por defecto también con variables en el fichero config.toml

    defaultContentLanguage = 'es'

En el caso de learn la página que nos muestra, si no hay contenido en la carpeta content, es el contenido del fichero index.html Si entramos en él, y así vemos cómo utilizar la estructura de control en una plantilla, vemos claramente dónde se ubica la traducción, ya que por defecto, esta plantilla está preparada para inglés y francés. Añadamos el español. Para ello observa y utiliza la estructura de controlc if - else if - end sintaxis estructuras de control.

También hay que realizar las modificaciones copiando los ficheros en la carpeta layout

    {{if eq .Site.Language.Lang "fr"}}
       <h1>Personaliser la page d'accueil</h1>
   
    {{else if eq .Site.Language.Lang "es" }}
       <h1>Personaliza tu página principal</h1>
   
    {{else if eq .Site.Language.Lang "en"}}
           <h1>Customize your own home page</h1>
    {{end}}




