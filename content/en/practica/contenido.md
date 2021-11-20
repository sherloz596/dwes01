---
title: "Content"
date: 2021-11-17T09:48:43+01:00
weight: 4
draft: false
---
***
To create new content we are going to generate text pages with markdown format.
We look at how we use different directories to create our organization of our content.

Each directory will correspond to a section.

Within each section there may be a _index.md file whose content will be displayed when we select the specific directory.

Command to create content files and/or sections:

    hugo new [section]/file.md

In the specific case of the learn template, the pages are classified into two types, those that are the head of a topic or section (_index.md) and those that have their content.

To create a page that is a chapter header (we create the theory section and the _index.md file):

    hugo new chapter --kind theory/_index.md


To create a file within the theory section

    hugo new chapter --kind theory/topic1.md

When we generate content, the files created we see that in the header or first lines they can have meta-information This information goes between three lines and constitutes what is called the **front matter** of the page. In this section we will give values ​​to variables that are later can use.

Of the different values, we are interested in seeing some that are usually in the archtypes and usually appear by default:

+ **title** will be the title that this page will have to be referenced in the different menus
+ **weight** is one of the ways to order the pages and sections.
+ **draft** Indicates if the page is true draft or not. If it is a draft, you will see us.
+ **description** It is a description that will appear on the main page or index of this section. It will appear for each page, unless it is specified that we do not want it. will display.



