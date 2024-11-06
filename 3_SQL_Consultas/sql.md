### 🐹 Consultas SQL Básica

<img src="3_SQL_Consultas/s_1.png" alt="consulta basica 1" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🐹 Consultas SQL Básica 2

<img src="3_SQL_Consultas/s_2.png" alt="consulta basica 2" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🏷️ Consultas SQL Intermedia

<img src="3_SQL_Consultas/s_3.png" alt="consulta intermedia" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🎁 Consultas SQL Avanzada

<img src="3_SQL_Consultas/s_4.png" alt="consulta avanzada" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### SELECT 📚

- **Título:** Navegando por tus Datos con `SELECT`
- **Subtítulo:** La clave para recuperar información en MySQL 🗝️

---

### * / COLUMNAS 📚

- Todas las columnas `SELECT *`
- Seleccionando las columnas `SELECT col1, col2, col3`

---

### Alias en las Columnas 📚

- Seleccionando las columnas `SELECT col1 as id, col2 as nombre, col3 as edad`

===

### FROM 📍

- Seleccionando las tablas con `FROM tabla1`
- Se pueden seleccionar varias tablas `FROM tabla1, tabla2`

---

### Alias en las Tablas 📚

- Usando el alias `FROM tabla1 as t1, tabla2 as t2`

===

### LIMIT 📍

- **`LIMIT`**: Restringe el número de filas que se devuelven en el conjunto de resultados.
- **Propósito**: Controlar la cantidad de datos retornados, optimizando el rendimiento y la legibilidad.

---

### Limit normal y con offset 📈

- Limit normal `SELECT * FROM tabla1 LIMIT 2`
- Limit con offset `SELECT * FROM tabla2 LIMIT 3,2`

===

### ORDER BY 📍

- **`ORDER BY`**: Ordena el conjunto de resultados según una o más columnas especificadas.
- **Propósito**: Presentar los datos de manera lógica y fácil de analizar.

---

### ORDER BY ASCENDENTE Y DESCENDENTE 📚

- Ascendente `SELECT * FROM tabla1 ORDER BY col1 ASC`
- Descendente `SELECT * FROM tabla1 ORDER BY col1 DESC`