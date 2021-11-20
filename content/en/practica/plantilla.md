---
title: "Template"
date: 2021-11-18T21:16:14+01:00
weight: 6
draft: false
---
***
We must identify the parts of a template. Regardless of the template used, we can talk about:

1. Logo
2. Colors used in the style
3. Main menu Let's identify those elements in our template and see how to modify them to customize it to our liking.

Logo

In this template, learn, the logo is loaded after a partial. The partial folder will contain html files that will be part of an html page, so that I can invoke them when I need them. For example a footer.html or a header.html

In this case the location is themes / layoout / partial / logo.html

Now what you have to do is copy the file in the layout directory and modify including the logo that we want it to have, which will be located in the static / images folder

We modify the file updating the logo that we want. In this case the logo is rendered from an svg element. We copy our logo in the static folder and specify it in an img element

For this we make a logo design. (there are many free websites for it)

Then we modify the logo.html file and replace the svg element with an img element

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
        Web development
    </a>

Menu

The menu is a very important section. In this template the menu will be located on the left side of the template. To add / modify it, we must specify it in the config.toml file, adding the elements [[menu.shortcuts]], for each item that we want to add. For example, we are going to add 3 items

    [[menu.shortcuts]]
    name="<i class='fab fa-php'></i>   php"
    identified=""
    url="https://php.net"
    weight=1

    [[menu.shortcuts]]
    name="<i class='fab fa-wikipedia-w'></i>   Course Wiki"
    identified=""
    url="https://es.wikieducator.org/Usuario:ManuelRomero/ProgramacionWeb/Contenido"
    weight=2

    [[menu.shortcuts]]
    name="<i class='far fa-question-circle'></i>   Solved exercises"
    identified=""
    url="http://manuel.infenlaces.com/dwes/ejercicios/"
    weight=3

Style

This template has up to three different color styles ready. To use them, simply set the corresponding value of the themeVariant variable in the config.toml configuration file. Allowed values ​​are red, green, blue

    [params]
    themeVariant = "blue" or "green" or "red"

Search

To modify this button we access our new theme-dwes.css and modify the variables that affect search, according to our taste

Home

To modify the home, we must do it from the configuration file. In this case, as we have the Spanish language configured, for the menu title, we must specify these variables within a language section. The modified parameters are as follows

    [Languages]
    [Languages.es]
    landingPageURL = "http://cpilosenlaces.com"
    landingPageName = "<i class='fas fa-university'></i> CPIFP Los Enlaces"

footer

The footer is this template, it corresponds to a partial, so we would have to access it, copy it to our directory and modify it. The file that shows the footer in the menu part is called menu-footer.html A small modification and we see the update on the page.
