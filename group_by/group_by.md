## Group By

- ¿Qué es GROUP BY?
- Sirve para agrupar datos que se repiten
- Se usa con funciones de agregación (Count(), Sum(), Avg()..)

---

## ¿Cuándo Usarlo?

Cuando quieras agrupar datos similares y obtener resultados agregados por grupo, por ejemplo:

- Sumar ventas por mes.
- Contar empleados por departamento.

---

## Código Ejemplo

```sql
SELECT  columna1, 
        columna2, 
        FUNCION_AGREGADA(columna3)
FROM tabla
GROUP BY columna1, columna2;
```
