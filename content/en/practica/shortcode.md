---
title: "Shortcode"
date: 2021-11-18T21:15:17+01:00
weight: 5
draft: false
---
***
A shortcode is a fragment of html code that will be rendered within an md file when the system loads or renders said content page. It is a way to give visual effects and to have more functionality within our website.

Some of the functions are:

+ Expand text.
{{%expand "Read more function" %}}One of the functions of shortcodes is to shorten/expand text{{% /expand%}}

+ Buttons.

{{% button href="http://www.cpilosenlaces.com/" icon="fas fa-graduation-cap" %}}CPIFP Los Enlaces{{% /button %}}

+ Mark text as news.
{{% notice note %}}
Mark text as news
{{% /notice %}}

+ Graphics with mermaid.

{{<mermaid align="left">}}
graph LR;
    A[Straight edge] -->|Link| B(Round edge)
    B --> C{Decision}
    C -->|A| D[Result A]
    C -->|B| E[Result B]
{{< /mermaid >}}

+ Tabs of different elements.
{{< tabs >}}
{{% tab name="Option 1" %}}
```Option 1
This is the content of the first tab
```
{{% /tab %}}
{{% tab name="Option 2" %}}
```Option 2
This is the content of the second tab
```
{{% /tab %}}
{{% tab name="Option 3" %}}
```Option 3
This is the content of the third tab
```
{{% /tab %}}
{{< /tabs >}}