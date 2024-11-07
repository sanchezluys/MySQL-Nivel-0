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

### * / COLUMNAS 📜

- Todas las columnas `SELECT *`
- Seleccionando las columnas `SELECT col1, col2, col3`

---

### Alias en las Columnas 🐔

- Seleccionando las columnas `SELECT col1 as id, col2 as nombre, col3 as edad`

===

### FROM 📍

- Seleccionando las tablas con `FROM tabla1`
- Se pueden seleccionar varias tablas `FROM tabla1, tabla2`

---

### Alias en las Tablas 📚

- Usando el alias `FROM tabla1 as t1, tabla2 as t2`

===

### LIMIT 👋

- **`LIMIT`**: Restringe el número de filas que se devuelven en el conjunto de resultados.
- **Propósito**: Controlar la cantidad de datos retornados, optimizando el rendimiento y la legibilidad.

---

### Limit normal y con offset 📈

- Limit normal `SELECT * FROM tabla1 LIMIT 2`
- Limit con offset `SELECT * FROM tabla2 LIMIT 3,2`

===

### ORDER BY 📝

- **`ORDER BY`**: Ordena el conjunto de resultados según una o más columnas especificadas.
- **Propósito**: Presentar los datos de manera lógica y fácil de analizar.

---

### ORDER BY ASCENDENTE Y DESCENDENTE ⚠️

- Ascendente `SELECT * FROM tabla1 ORDER BY col1 ASC`
- Descendente `SELECT * FROM tabla1 ORDER BY col1 DESC`

---

### ORDER BY MULTICOLUMNAS 🗃️

- Se puede aplicar a varias columnas 
- Ejemplo `SELECT * FROM tabla1 ORDER BY col1 ASC, col2 DESC`

===

### CONSULTA INTERMEDIA - WHERE 👀

- **`SELECT * FROM TABLA WHERE ID=10 ORDER BY ID ASC LIMIT 1`**: Filtrar y Ordenar Datos.
- **Propósito**: Obtener solo los datos que cumplan con condiciones especificas.

---

### LOGICAS BINARIAS - WHERE 🐶

- **`SELECT * FROM TABLA WHERE ID=10 ORDER BY ID ASC LIMIT 1`**: Filtrar y Ordenar Datos.
- **Propósito**: Obtener solo los datos que cumplan con condiciones especificas.

---

### USO DE FUNCIONES 🧑‍🎄

<img src="3_SQL_Consultas/fun_2.jpg" alt="funciones" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### USO DE FUNCIONES 2 🧑‍🎄

<img src="3_SQL_Consultas/fun_1.png" alt="funciones2" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### TIPOS DE FUNCIONES 📊 🧠

- **Numéricas**: ABS(), CEIL(), FLOOR(), ROUND() 🧮
- **Manipulación** de cadenas: CONCAT(), CONCAT_WS(), LOWER() 📝
- **Fechas** y Horas: NOW(), CURDATE(), DATE_FORMAT() 🕰️
- **Lógicas** y Condicionales: IF(), CASE WHEN, COALESCE() 🤔

---

### Funciones Numéricas 🧮

Las funciones numéricas en SQL nos permiten realizar operaciones matemáticas básicas y avanzadas. Algunas de las más comunes son:

- `ABS(x)`: Devuelve el valor absoluto de un número.
- `CEIL(x)`: Devuelve el siguiente entero más grande que el número dado.
- `FLOOR(x)`: Devuelve el entero más grande que es menor o igual que el número dado.
- `ROUND(x, [d])`: Redondea un número al número de decimales especificado. Si no se especifica d, se redondea al entero más cercano.

Ejemplo:

```sql
SELECT 
    ABS(-10.5) AS valor_absoluto,
    CEIL(3.14) AS techo,
    FLOOR(3.14) AS piso,
    ROUND(3.14159, 2) AS redondeado
FROM dual;
```

---

### Funciones de Manipulación de Cadenas 📝

Las funciones de manipulación de cadenas en SQL nos permiten trabajar con texto. Algunas de las más útiles son:

- `CONCAT(str1, str2, ...)`: Concatena dos o más cadenas de texto.
- `CONCAT_WS(separator, str1, str2, ...)`: Concatena dos o más cadenas de texto con un separador personalizado.
- `LOWER(str)`: Convierte una cadena de texto a minúsculas.

Ejemplo:

```sql
SELECT
    CONCAT('Hola', ', ', 'mundo') AS concatenado,
    CONCAT_WS(' - ', 'Curso', 'de', 'SQL') AS concatenado_con_separador,
    LOWER('SQL es GENIAL') AS texto_a_minusculas
FROM dual;
```

---

### Funciones de Fecha y Hora 🕰️

Las funciones de fecha y hora en SQL nos permiten trabajar con información temporal. Algunas de las más comunes son:

- `NOW()`: Devuelve la fecha y hora actual.
- `CURDATE()`: Devuelve la fecha actual.
- `DATE_FORMAT(date, format)`: Formatea una fecha según un patrón especificado.

Ejemplo:

```sql
SELECT
    NOW() AS fecha_y_hora_actual,
    CURDATE() AS fecha_actual,
    DATE_FORMAT(NOW(), '%d/%m/%Y') AS formato_personalizado
FROM dual;
```

---

### Funciones Lógicas y Condicionales 🤔

Las funciones lógicas y condicionales en SQL nos permiten realizar operaciones basadas en condiciones. Algunas de las más útiles son:

- `IF(condition, true_value, false_value)`: Devuelve un valor si la condición es verdadera, y otro valor si es falsa.
- `CASE WHEN condition THEN value END`: Evalúa una serie de condiciones y devuelve un valor correspondiente.
- `COALESCE(value1, value2, ...)`: Devuelve el primer valor no nulo de la lista.

Ejemplo:

```sql
SELECT
    IF(10 > 5, 'Verdadero', 'Falso') AS resultado_if,
    CASE 
        WHEN 3 > 1 THEN 'Mayor'
        WHEN 3 < 1 THEN 'Menor'
        ELSE 'Igual'
    END AS resultado_case,
    COALESCE(NULL, 'Valor por defecto', 'Otro valor') AS resultado_coalesce
FROM dual;
```