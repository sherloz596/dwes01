---
title: "Plantilla"
date: 2021-11-18T21:16:14+01:00
weight: 6
draft: false
---
***
Debemos identificar las partes de una plantilla. Independientemente de la plantilla utilizada podemos hablar de:

1. Logo
2. Colores usados en el estilo
3. Menú principal Identifiquemos esos elementos en nuestra plantilla y veamos cómo modificarlos para personalizarla a nuestro gusto.

Logo

En esta plantilla, learn, el logo se carga a patir de un partial. La carpeta partial , va a contener ficheros html que serán parte una página html, de forma que los podré invocar cuando los necesite. Por ejemplo un footer.html o un header.html

En este caso la ubicación es themes/layoout/partial/logo.html

Ahora lo que hay que hacer es copiar el fichero en el directorio layout y modificar incluyendo el logo que queremos que tenga, que irá ubicado en la carpeta static/images 

Modificamos el fichero actualizando al logo que queramos. En este caso el logo se rederiza a partir de un elemento svg . Copiamos nuestro logo en la carpeta static y lo especificamos en un elemento img

Para ello hacemos un diseño de logo. (hay muchas web gratuitas para ello)

Luego modificamos el fichero logo.html y sustituimos el elemento svg por un elemento img 

    <a id="logo"
        href="{{ .Site.Params.landingPageURL | default "/" | relLangURL }}"
        style="
        color: #3d414d;
        font-family: 'Novacento Sans Wide', 'Helvetica', 'Tahoma', 'Geneva', 'Arial', sans-serif;
        font-size: 30px;
        font-weight: bold;
        margin-top: -2px;
        ">
        <img src="/images/logo.png" alt="Logo del ciclo">
        Desarrollo Web
    </a>

Menú

El menú es una sección muy importante. En esta plantilla el menú va a estar ubicado en la parte izquierda de la plantilla. Para añadir/modificarlo, debemos especificarlo en el fichero config.toml , añádiendo los elementos [[menu.shortcuts]] , para cada item que queremos añadir. Por ejemplo, vamos a añadir 3 items

    [[menu.shortcuts]]
    name="<i class='fab fa-php'></i>   Lenguaje php"
    identified=""
    url="https://php.net"
    weight=1

    [[menu.shortcuts]]
    name="<i class='fab fa-wikipedia-w'></i>   Wiki del curso"
    identified=""
    url="https://es.wikieducator.org/Usuario:ManuelRomero/ProgramacionWeb/Contenido"
    weight=2

    [[menu.shortcuts]]
    name="<i class='far fa-question-circle'></i>   Ejercicios resueltos"
    identified=""
    url="http://manuel.infenlaces.com/dwes/ejercicios/"
    weight=3

Estilo

Esta plantilla tiene hasta tres estilos de colores diferentes preparados. Para utilizarlos basta con establecer el valor correspondiente de la variable themeVariant en el fichero de configuración config.toml . Los valores permitidos son red, green, blue

    [params]
    themeVariant = "blue" or "green" or "red"

Search

Para modificar este botón accedemos a nuestro nuevo theme-dwes.css y modificamos las variables que afectan a search, según nuestro gusto

Home

Para modificar el home, debemos hacerlo desde el fichero de configuración. En este caso, como tenemos configurado el idioma español, para el título del menú, debemos especificar estas variables dentro de una sección de lenguaje Los parámetros modificados son los siguientes

    [Languages]
    [Languages.es]
    landingPageURL = "http://cpilosenlaces.com"
    landingPageName = "<i class='fas fa-university'></i> CPIFP Los Enlaces"

footer

El footer es esta plantilla, corresponde a un partial, por lo que tendríamos que acceder a él, copiarlo en nuestro directorio y modificarlo. El fichero que muestra el footer en la parte del menú se llama menu-footer.html Una pequeña modificación y observamos la actualización en la página 
