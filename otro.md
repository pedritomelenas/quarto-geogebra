---
title: La clase de funciones
lang: es
format:
   html:
      toc: false
      html-math-method: mathjax
      css: styles.css
      include-before-body: includes-header.html
---


## Pintar funciones
Para obtener el polinomio interpolador de unos puntos:
```
f(x)=Polinomio({(0,0),(2,3),(6,2),(9,4)})
```

Para obtener la tangente de una función que pasa por un punto:
```
Tangente(A, f)
```
## Hacer secuencias

Con `Secuencia` podemos obtener una lista. El primer argumento es la expresión de la lista, el segundo la variable, el tercero el valor inicial, el cuarto el valor final, y el quinto el incremento. 

```
Secuencia((i,0),i,0,n,1)
```

Podemos dividir el intervalo $[A(1)-\delta, A(1)+\delta]$ en $n$ trozos iguales con el siguiente código:

```
P=Secuencia((i, 0), i, x(A) - δ, x(A) + δ, 2δ / n)
```

Utilizando esta lista P, podemos dibujar una secuencia de polígonos con la que realizaremos la aproximación de la integral por el método del polígono.

```
Secuencia(Polígono((x(P(j)), 0), (x(P(j)), f(x(P(j)))), 
(x(P(j - 1)), f(x(P(j - 1)))), (x(P(j - 1)), 0)), j, 2, n + 1, 1)
```

Utilizaremos esta secuencia para, aumentando el valor $n$, obtener una aproximación por este método de la integral.

## Enlaces

Podéis obtener [geogebra](https://geogebra.org) en este [enlace](https://geogebra.org/download)

## Matemáticas

En línea $x^2+1$ 

$$
\int_a^b x^2+1\, dx
$$


<div id="ggbApplet"></div>


<script>
var parameters = {
"id": "ggbApplet",
"width":800,
"height":500,
// use this instead of ggbBase64 to load a material from geogebra.org
// "material_id":12345,
// "ggbBase64":"",
// use this instead of ggbBase64 to load a .ggb file
"filename":"assets/integracion-trapecio.ggb"};
// is3D=is 3D applet using 3D view, AV=Algebra View, SV=Spreadsheet View, CV=CAS View, EV2=Graphics View 2, CP=Construction Protocol, PC=Probability Calculator, DA=Data Analysis, FI=Function Inspector, PV=Python, macro=Macro View
var views = {'is3D': 0,'AV': 0,'SV': 1,'CV': 1,'EV2': 0,'CP': 0,'PC': 0,'DA': 0,'FI': 0,'macro': 0};
var applet = new GGBApplet(parameters, '5.0',views); //poner views como tercer argumento si queremos habilitarlo
window.onload = function() {
    applet.inject('ggbApplet')  
};
</script>