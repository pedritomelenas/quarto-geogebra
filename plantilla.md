---
title: Plantilla ejemplo
lang: es
format:
   html:
      toc: true
      html-math-method: mathjax
      css: styles.css
      include-before-body: includes-header.html
---


## Ejemplo GeoGebra

Yo puedo escribir aquí lo que me venga en gana.

<div id="ggbApplet"></div>


<script>
var parameters = {
"id": "ggbApplet",
"width":900,
"height":702,
// use this instead of ggbBase64 to load a material from geogebra.org
// "material_id":12345,
// "ggbBase64":"",
// use this instead of ggbBase64 to load a .ggb file
"filename":"/assets/geogebra/hueso-nazari-tesela.ggb"};
// is3D=is 3D applet using 3D view, AV=Algebra View, SV=Spreadsheet View, CV=CAS View, EV2=Graphics View 2, CP=Construction Protocol, PC=Probability Calculator, DA=Data Analysis, FI=Function Inspector, PV=Python, macro=Macro View
var views = {'is3D': 0,'AV': 1,'SV': 1,'CV': 1,'EV2': 0,'CP': 0,'PC': 0,'DA': 0,'FI': 0,'macro': 0};
var applet = new GGBApplet(parameters, '5.0',views); //poner views como tercer argumento si queremos habilitarlo
window.onload = function() {
    applet.inject('ggbApplet')  
};
</script>



