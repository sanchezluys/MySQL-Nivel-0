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

---

### Código Ejemplo

<section data-auto-animate>
	<pre data-id="code-animation">
    <code class="hljs javascript" data-trim data-line-numbers>
		SELECT  columna1, 
                columna2, 
                FUNCION_AGREGADA(columna3)
        FROM tabla
        GROUP BY columna1, columna2;
	</code></pre>
</section>