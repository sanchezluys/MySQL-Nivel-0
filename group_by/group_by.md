## Group By

- ¿Qué es GROUP BY?
- Sirve para agrupar datos que se repiten
- Se usa con funciones de agregación (Count(), Sum(), Avg()..)

<!-- This presentation dshowcases examples created with the [reveal.js plugin collection](https://github.com/rajgoel/reveal.js-plugins). -->

---

### ¿Cuándo Usarlo?

Cuando quieras agrupar datos similares y obtener resultados agregados por grupo, por ejemplo:

- Sumar ventas por mes.
- Contar empleados por departamento.

===

## Ejemplos

---

### Interactive elements

<section data-auto-animate>
	<h2 data-id="code-title">Código para MySQL</h2>
	<pre data-id="code-animation">
    <code class="hljs javascript" data-trim data-line-numbers>
		SELECT  columna1, 
                columna2, 
                FUNCION_AGREGADA(columna3)
        FROM tabla
        GROUP BY columna1, columna2;
	</code></pre>
</section>

---

### Interactive elements2

<div class="anything">
<!-- { "initialize": "function(container,options) {globe(container);}" } -->
</div>

---

### Charts

<div style="height:480px">
<canvas data-chart="pie">
,Black, Red, Green, Yellow
My first dataset, 40, 40, 20, 6
My second dataset, 45, 40, 25, 4
</canvas>
</div>

---

<!-- .slide: data-fullscreen="true"  -->

### Embedded online content

<iframe class="stretch" src="https://www.youtube.com/embed/5xAgp6i9lUQ?rel=0" frameborder="0" allowfullscreen></iframe>

===

## Open source

You can find the source code of

- the presentation framework [here](https://github.com/hakimel/reveal.js)&nbsp;
<iframe src="https://ghbtns.com/github-btn.html?user=hakimel&repo=reveal.js&type=star&count=true&size=large" frameborder="0" scrolling="0" width="170" height="30" title="GitHub"></iframe>
- the plugin collection [here](https://github.com/rajgoel/reveal.js-plugins)&nbsp;
<iframe src="https://ghbtns.com/github-btn.html?user=rajgoel&repo=reveal.js-plugins&type=star&count=true&size=large" frameborder="0" scrolling="0" width="170" height="30" title="GitHub"></iframe>
- the demo presentations [here](https://github.com/rajgoel/reveal.js-demos)&nbsp;
<iframe src="https://ghbtns.com/github-btn.html?user=rajgoel&repo=reveal.js-demos&type=star&count=true&size=large" frameborder="0" scrolling="0" width="170" height="30" title="GitHub"></iframe>
