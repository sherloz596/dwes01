---
title: "Contenido"
date: 2021-11-17T09:48:43+01:00
weight: 4
draft: false
---
***
Para crear nuevo contenido vamos a generar páginas de texto con formato markdown.
Observamos cómo usamos diferentes directorios para crear nuestra organización de nuestro contenido.

Cada directorio corresponderá a una sección.

Dentro de cada sección puede haber un fichero _index.md cuyo contenido se visualizará cuando seleccionemos el directorio concreto.

Comando para crear ficheros de contenido y/o secciones:

    hugo new [seccion]/fichero.md

En el caso concreto de la plantilla learn,se clasifica las páginas en dos tipos, las que son cabecera de un tema o sección (_index.md) y las que tienen contenido de las mismas.

Para crear una página que es cabecera de capítulo (creamos la sección teoría y el fichero _index.md):

    hugo new chapter --kind teoria/_index.md


Para crear un fichero dentro de la sección teoría

    hugo new chapter --kind teoria/tema1.md

Cuando generamos contenidos, los ficheros creados vemos que en la cabecera o primeras líneas pueden tener metainformación Esta información va entre tres líneas y constituye lo que se llama el **front matter** de la página En esta sección daremos valores a variables que luego se pueden utilizar.

De los diferentes valores, nos interesa ver alguno que suele estar en el archtypes y suelen aparecer por defecto:

+ **title** será el título que va a tener esta página para referenciarse en los diferentes menús
+ **weight** es una de las formas de ordenar las páginas y secciones.
+ **draft** Indica si la página es borrador true o no. En caso de ser borrador nos e visualizará.
+ **description** Es una descripcion que aparecerá en la página principal o index de esta sección. Aparecerá para cada página, salvo que se especifique que no lo queramos. visualizará.

