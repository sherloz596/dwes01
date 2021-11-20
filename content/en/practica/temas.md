---
title: "Themes"
date: 2021-11-16T20:26:52+01:00
weight: 3
draft: false
---
***
We have different ways to install a template.

All of them have to leave in the themes folder of our project a folder with the development of the template that we are going to download from git

The ways to get this folder can be:

1. Download the development and unzip it in the folder
2. Clone directly to the folder with git clone
3. Clone it as a submodule from the project folder

I have used the third way. To do this from the project directory, I have first created an empty repository:

    git init

After I have cloned it as a sub-module:

    git submodule add https://github.com/matcornic/hugo-theme-learn.git themes/learn

Finally I have modified the configuration file config.toml indicating the location of the theme:

    theme = 'learn'


