---
title: "Temas"
date: 2021-11-16T20:26:52+01:00
weight: 3
draft: false
---
***
Tenemos diferentes modos de instalar una plantilla.

Todas ellas han de dejar en la carpeta themes de nuestro proyecto una carpeta con el desarrollo de la plantilla que nos vamos a descargar de git

Las formas de obtener esta carpeta puede ser:

1. Descargar el desarrollo y descomprimirlo en la carpeta
2. Clonar directamente en el carpeta con git clone
3. Clonarlo como un submodule a partir de la carpeta del proyecto

Yo he utilizado la tercera forma. Para ello desde el directorio del proyecto, primero he creado un repositorio vacio:

    git init

Después lo he clonado como un submodulo:

    git submodule add https://github.com/matcornic/hugo-theme-learn.git themes/learn

Finalmente he modificado el fichero de configuración config.toml indicando la ubicación del tema:

    theme = 'learn'


