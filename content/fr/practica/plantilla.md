---
title: "Modèle"
date: 2021-11-18T21:16:14+01:00
weight: 6
draft: false
---
***
Nous devons identifier les parties d'un modèle. Quel que soit le modèle utilisé, on peut parler de :

1. Logo
2. Couleurs utilisées dans le style
3. Menu principal Identifions ces éléments dans notre modèle et voyons comment les modifier pour le personnaliser à notre guise.

Logo

Dans ce modèle, apprenez, le logo est chargé après un partiel. Le dossier partiel contiendra des fichiers html qui feront partie d'une page html, afin que je puisse les appeler quand j'en ai besoin. Par exemple un footer.html ou un header.html

Dans ce cas, l'emplacement est theme / layout / partial / logo.html

Maintenant, ce que vous avez à faire est de copier le fichier dans le répertoire de mise en page et de modifier notamment le logo que nous voulons qu'il ait, qui sera situé dans le dossier static / images

Nous modifions le fichier mettant à jour le logo que nous voulons. Dans ce cas, le logo est rendu à partir d'un élément svg. Nous copions notre logo dans le dossier statique et le spécifions dans un élément img

Pour cela, nous réalisons un design de logo. (il existe de nombreux sites gratuits pour cela)

Ensuite, nous modifions le fichier logo.html et remplaçons l'élément svg par un élément img 

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
        Développement web
    </a>

Menu

Le menu est une section très importante. Dans ce modèle, le menu sera situé sur le côté gauche du modèle. Pour l'ajouter/modifier, il faut le préciser dans le fichier config.toml, en ajoutant les éléments [[menu.shortcuts]], pour chaque élément que l'on souhaite ajouter. Par exemple, nous allons ajouter 3 éléments

    [[menu.shortcuts]]
    name="<i class='fab fa-php'></i>   php"
    identified=""
    url="https://php.net"
    weight=1

    [[menu.shortcuts]]
    name="<i class='fab fa-wikipedia-w'></i>   Wiki du cours"
    identified=""
    url="https://es.wikieducator.org/Usuario:ManuelRomero/ProgramacionWeb/Contenido"
    weight=2

    [[menu.shortcuts]]
    name="<i class='far fa-question-circle'></i>   Exercices résolus"
    identified=""
    url="http://manuel.infenlaces.com/dwes/ejercicios/"
    weight=3

Style

Ce modèle contient jusqu'à trois styles de couleurs différents. Pour les utiliser, il suffit de définir la valeur correspondante de la variable themeVariant dans le fichier de configuration config.toml. Les valeurs autorisées sont rouge, vert, bleu

    [params]
    themeVariant = "blue" or "green" or "red"

Chercher

Pour modifier ce bouton nous accédons à notre nouveau theme-dwes.css et modifions les variables qui affectent la recherche, selon notre goût

Home

Pour modifier le home, il faut le faire à partir du fichier de configuration. Dans ce cas, comme nous avons configuré la langue espagnole, pour le titre du menu, nous devons spécifier ces variables dans une section de langue. Les paramètres modifiés sont les suivants

    [Languages]
    [Languages.es]
    landingPageURL = "http://cpilosenlaces.com"
    landingPageName = "<i class='fas fa-university'></i> CPIFP Los Enlaces"

footer

Le pied de page est ce modèle, il correspond à un partiel, il faudrait donc y accéder, le copier dans notre répertoire et le modifier. Le fichier qui affiche le pied de page dans la partie menu s'appelle menu-footer.html Une petite modification et on voit la mise à jour sur la page. 
