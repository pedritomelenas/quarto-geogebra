---
title: Plantilla ejemplo
lang: es
language:
    es: 
        title-block-author-single: "Autores"
author: La clase de Matemáticas Dinámicas
format:
   html:
      toc: false
      html-math-method: mathjax
      css: styles.css
      include-before-body: includes-header.html
---

Queremos probar el siguiente enunciado, conocido como el *teorema de la amistad*.

>En cualquier grupo de seis personas existen siempre tres que se conocen mutuamante, o que se desconocen entre sí.




::: {.callout-note}

Es útil abordar este problema con la terminología de grafos. Se considera un grafo con 6 vértices, donde cada vértice es una persona distinta, y los segmentos que los unen son las relaciones entre ellos. A este tipo de grafo se le conoce como grafo completo. En particular, cuando un grafo tiene $n$ vértices y cada par de vértices está conectado, se le denota como $K_n$.

:::


::: {.callout-tip}

Por ejemplo, un grafo completo de 3 vértices se representa como $K_3$, o como un ciclo de longitud 3 $C_3$, conocido como triángulo.

:::


Se considera ahora un $K_6$, que tiene un total de 15 aristas. Si se colorean las aristas con rojo o verde dependiendo de si las personas representadas por los vértices incidentes son conocidas o desconocidas entre sí, respectivamente, el *teorema de la amistad* establece lo siguiente:

> Independientemente de cómo se coloreen las aristas de $K_6$ con rojo o verde, siempre habrá un triángulo rojo, es decir, un conjunto de tres personas que son mutuamente desconocidas, o un triángulo verde, que representa tres personas que se conocen entre sí.


::: {#thm-seis-desconocidos}

Cualquier coloración de $K_6$ con dos colores tiene al menos un  triángulo ($C_3$) cuyos lados son del mismo color.
:::



::: {.proof}

Se elige uno de los vértices $P$ de $K_6$. Existen cinco aristas incidentes sobre $P$. Cada una de estas aristas está coloreada con color rojo (desconocidos) o verde (conocidos). Aplicamos el *Principio del Palomar* que nos asegura que, al menos, tres aristas son del mismo color.

::: {layout-ncol=2}

![](assets/Imagen1.svg){width=60%}

![](assets/Teorema_amistad_2.svg){width=60%}

:::

Sean $A,B,C$ los otros vértices opuestos a $P$ de estas tres aristas del mismo color, supongamos que son de color rojo. Si alguna de las aristas $AB,AC,BC$ es roja, junto a las aristas incidentes sobre $P$ se encuentra el triángulo rojo (personas desconocidas entre sí). 

![](assets/Imagen4.svg){width=30%}


Si ninguna de las 3 aristas anteriores es roja, se tiene que las 3 son verdes obteniendo un triángulo de color verde $ABC$ (personas mutuamente conocidas).



![](assets/imagen3.svg){width=30%}

:::


En la siguiente aplicación, pulsa "Recalcular" para colorear los lados de forma aleatoria en rojo y azul.

<div id="ggbApplet"></div>


<script>
var parameters = {
"id": "ggbApplet",
"width":600,
"height":500,
// use this instead of ggbBase64 to load a material from geogebra.org
// "material_id":12345,
// "ggbBase64":"",
// use this instead of ggbBase64 to load a .ggb file
"filename":"assets/conocidos-desconocidos.ggb"};
// is3D=is 3D applet using 3D view, AV=Algebra View, SV=Spreadsheet View, CV=CAS View, EV2=Graphics View 2, CP=Construction Protocol, PC=Probability Calculator, DA=Data Analysis, FI=Function Inspector, PV=Python, macro=Macro View
var views = {'is3D': 0,'AV': 0,'SV': 1,'CV': 1,'EV2': 0,'CP': 0,'PC': 0,'DA': 0,'FI': 0,'macro': 0};
var applet = new GGBApplet(parameters, '5.0',views); //poner views como tercer argumento si queremos habilitarlo
window.onload = function() {
    applet.inject('ggbApplet')  
};
</script>



