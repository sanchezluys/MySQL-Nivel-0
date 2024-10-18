#### 🌐 Introducción

<img src="0_Introduccion/meet_1.png" alt="meet"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;">

---

#### 🎯 Objetivos

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🗄️ Bases de datos Relacionales</strong>: Comprender la estructura de datos en tablas relacionadas.
</p>
<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>📊 Tablas</strong>: Crear y gestionar tablas de forma eficiente.
</p>
<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>🔗 Relaciones entre tablas</strong>: Establecer relaciones mediante claves primarias y foráneas.
</p>
<p class="fragment" data-fragment-index="4" style="text-align: left;">
  4. <strong>🛠️ CRUD</strong>: Realizar operaciones básicas (Crear, Leer, Actualizar, Eliminar) en las tablas.
</p>
<p class="fragment" data-fragment-index="5" style="text-align: left;">
  5. <strong>🔍 Consultas SQL</strong>: Ejecutar consultas para recuperar y manipular datos.
</p>
<p class="fragment" data-fragment-index="6" style="text-align: left;">
  6. <strong>🚀 Publicar en GitHub</strong>: Desarrollar y publicar una base de datos en GitHub.
</p>

---

#### ⏳ Meta Final Proyecto en GitHub

<img src="0_Introduccion/git.webp" alt="git"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Requisitos

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>💻 Computadora</strong>: Un equipo adecuado para desarrollar y gestionar bases de datos.
</p>
<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🌐 Conexión a Internet</strong>: Esencial para colaborar, acceder a recursos y gestionar proyectos en la nube.
</p>
<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>☁️ Servidor con MySQL en la nube</strong>: Un entorno de base de datos accesible y escalable para alojar proyectos.
</p>
<p class="fragment" data-fragment-index="4" style="text-align: left;">
  4. <strong>💻 MySQL Workbench</strong>: Herramienta para diseñar, modelar y gestionar bases de datos.
</p>
<p class="fragment" data-fragment-index="5" style="text-align: left;">
  5. <strong>🌐 GitHub</strong>: Plataforma para compartir, colaborar y versionar proyectos.
</p>
<p class="fragment" data-fragment-index="6" style="text-align: left;">
  6. <strong>🧑‍🤝‍🧑 Trabajo en equipo</strong>: Colaboración activa con otros desarrolladores para mejorar la eficiencia y calidad del proyecto.
</p>
<p class="fragment" data-fragment-index="7" style="text-align: left;">
  7. <strong>⚙️ Metodologías ágiles</strong>: Uso de enfoques como Scrum o Kanban para gestionar el desarrollo de manera eficiente.
</p>
<p class="fragment" data-fragment-index="8" style="text-align: left;">
  8. <strong>📚 Ganas de aprender</strong>: Actitud proactiva para adquirir nuevos conocimientos y mejorar continuamente.
</p>

===

#### 📊 Introducción a un Proyecto Desarrollo IT

<img src="img/herr_avan/v_1.png" alt="vista 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 FrontEnd

<img src="img/herr_avan/v_2.png" alt="vista 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 BackEnd

```sql

CREATE 
        ALGORITHM = UNDEFINED 
        DEFINER = `credicel_profesor`@`%` 
        SQL SECURITY DEFINER
VIEW    `lista` AS
        SELECT 
            `Dpto`.`departamento` AS `DEPARTAMENTO`,
            `Mcipio`.`municipio` AS `MUNICIPIOS`
        FROM
            (`departamentos` `Dpto`
            JOIN `municipios` `Mcipio` 
                ON (`Dpto`.`id_departamento` = `Mcipio`.`departamento_id`))

```

===

#### 🛠️ Entendiendo las Funciones

<img src="img/herr_avan/f/f_1.png" alt="Funcion 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Partes de las Funciones

<img src="img/herr_avan/f/f_2.png" alt="funcion 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Código Básico Ejemplo para una Función

```sql

DELIMITER $$

CREATE FUNCTION nombre_completo(nombre VARCHAR(50), apellido VARCHAR(50))
RETURNS VARCHAR(101)
DETERMINISTIC
BEGIN
    RETURN CONCAT(nombre, ' ', apellido);
END $$

DELIMITER ;

```

---

#### 🛠️ Código Intermedio Ejemplo para una Función

```sql

DELIMITER $$

CREATE FUNCTION format_full_name(first_name VARCHAR(50), 
                                middle_name VARCHAR(50), 
                                last_name VARCHAR(50))
RETURNS VARCHAR(151)
DETERMINISTIC
BEGIN
    DECLARE full_name VARCHAR(151);
    
    -- Inicializa full_name como una cadena vacía
    SET full_name = '';
    
    -- Si el primer nombre no es nulo, agregarlo
    IF first_name IS NOT NULL THEN
        SET full_name = first_name;
    END IF;
    
    -- Si el segundo nombre no es nulo, agregarlo con un espacio
    IF middle_name IS NOT NULL THEN
        SET full_name = CONCAT(full_name, ' ', middle_name);
    END IF;
    
    -- Si el apellido no es nulo, agregarlo con un espacio
    IF last_name IS NOT NULL THEN
        SET full_name = CONCAT(full_name, ' ', last_name);
    END IF;
    
    -- Retorna el nombre completo, eliminando espacios en blanco adicionales
    RETURN TRIM(full_name);
END $$

DELIMITER ;


```

===

#### 🌀 Entendiendo los Procedimientos

<img src="img/herr_avan/p/p_1.png" alt="procedimiento 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Partes de los Procedimientos

<img src="img/herr_avan/p/p_2.png" alt="procedimiento 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Código Básico Ejemplo para un Procedimiento

```sql

DELIMITER $$

CREATE PROCEDURE insertarCliente(
    IN p_nombre VARCHAR(50),
    IN p_email VARCHAR(50),
    IN p_telefono VARCHAR(15)
)
BEGIN
    -- Insertar un nuevo cliente en la tabla "clientes"
    INSERT INTO clientes (nombre, email, telefono)
    VALUES (p_nombre, p_email, p_telefono);
END$$

DELIMITER ;

```

---

#### 🌀 Código Intermedio Ejemplo para una los Procedimientos

```sql

DELIMITER $$

CREATE PROCEDURE actualizarOInsertarCliente(
    IN p_id INT,
    IN p_nombre VARCHAR(50),
    IN p_email VARCHAR(50),
    IN p_telefono VARCHAR(15)
)
BEGIN
    DECLARE cliente_existe INT DEFAULT 0;

    -- Verificar si el cliente ya existe
    SELECT COUNT(*) INTO cliente_existe
    FROM clientes
    WHERE id = p_id;

    IF cliente_existe > 0 THEN
        -- Actualizar la información del cliente existente
        UPDATE clientes
        SET nombre = p_nombre, email = p_email, telefono = p_telefono
        WHERE id = p_id;
        SELECT 'Cliente actualizado' AS mensaje;
    ELSE
        -- Insertar un nuevo cliente
        INSERT INTO clientes (nombre, email, telefono)
        VALUES (p_nombre, p_email, p_telefono);
        SELECT 'Cliente insertado' AS mensaje;
    END IF;
END$$

DELIMITER ;

```