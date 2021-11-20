---
title: "Shortcode"
date: 2021-11-18T21:15:17+01:00
weight: 5
draft: false
---
***
Un shortcode est un fragment de code html qui sera rendu dans un fichier md lorsque le système chargera ou affichera ladite page de contenu. C'est un moyen de donner des effets visuels et d'avoir plus de fonctionnalités sur notre site Web.

Certaines des fonctions sont :

+ Développer le texte.
{{%expand "En savoir plus fonction" %}}L'une des fonctions des shortcodes est de raccourcir/étendre le texte{{% /expand%}}

+ Boutons.

{{% button href="http://www.cpilosenlaces.com/" icon="fas fa-graduation-cap" %}}CPIFP Los Enlaces{{% /button %}}

+ Marquez le texte comme actualité.
{{% notice note %}}
Marquez le texte comme actualité.
{{% /notice %}}

+ Graphiques avec mermaid.

{{<mermaid align="left">}}
graph LR;
    A[Bord droit] -->|Lien| B(bord arrondi)
    B --> C{Décision}
    C -->|A| D[Résultat A]
    C -->|B| E[Résultat B]
{{< /mermaid >}}

+ Tabs de différents éléments.

{{< tabs >}}
{{% tab name="Option 1" %}}
```Option 1
C'est le contenu du premier tab
```
{{% /tab %}}
{{% tab name="Option 2" %}}
```Option 2
C'est le contenu du deuxième tab
```
{{% /tab %}}
{{% tab name="Option 3" %}}
```Option 3
C'est le contenu du troisième tab
```
{{% /tab %}}
{{< /tabs >}}