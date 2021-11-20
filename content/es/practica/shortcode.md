---
title: "Shortcode"
date: 2021-11-18T21:15:17+01:00
weight: 5
draft: false
---
***
Un shortcode es un fragmento de código html que será renderizado dentro de un fichero md cuando el sistema cargue o renderice dicha página de contenido Es una forma de dar efectos visuales y de poder tener mayor funcionalidad dentro de nuestro sitio web.

Algunas de las funciones son:

+ Expandir texto.
{{%expand "Función leer más" %}}Una de las funciones de los shortcode es acortar/expandir texto{{% /expand%}}

+ Botones.

{{% button href="http://www.cpilosenlaces.com/" icon="fas fa-graduation-cap" %}}CPIFP Los Enlaces{{% /button %}}

+ Remarcar texto como una noticia.
{{% notice note %}}
Remarcar texto como una noticia
{{% /notice %}}

+ Gráficos con mermaid.

{{<mermaid align="left">}}
graph LR;
    A[Borde recto] -->|Enlace| B(Borde redondo)
    B --> C{Decisión}
    C -->|A| D[Resultado A]
    C -->|B| E[Resultado B]
{{< /mermaid >}}

+ Tabs de diferentes elementos.

{{< tabs >}}
{{% tab name="Opción 1" %}}
```Opción 1
Este es el contenido del primer tab
```
{{% /tab %}}
{{% tab name="Opción 2" %}}
```Opción 2
Este es el contenido del segundo tab
```
{{% /tab %}}
{{% tab name="Opción 3" %}}
```Opción 3
Este es el contenido del tercer tab
```
{{% /tab %}}
{{< /tabs >}}