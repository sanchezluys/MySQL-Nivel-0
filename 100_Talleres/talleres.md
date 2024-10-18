#### Talleres

<img src="100_Talleres/talleres_1.jpg" alt="talleres_1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;">

===

#### 🌐 Interfaces para MySQL - Workbench

<img src="100_Talleres/workbench_1.jpg" alt="workbench_1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;">

---

#### 📊 Instalando Workbench

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>💻 Descargar MySQL Workbench</strong>: Ve al sitio oficial de MySQL para <a href="https://dev.mysql.com/downloads/workbench/" target="_blank">descargar MySQL Workbench</a>. Asegúrate de seleccionar la versión compatible con tu sistema operativo (Windows, macOS, Linux).
</p>
<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>📥 Instalar MySQL Workbench</strong>: Ejecuta el instalador descargado y sigue las instrucciones en pantalla. Acepta los términos y elige las opciones de instalación predeterminadas o personalizadas según tus necesidades.
</p>
<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>🔧 Configurar MySQL Workbench</strong>: Una vez instalado, abre MySQL Workbench. En la pantalla principal, selecciona la opción para crear una nueva conexión con tu servidor MySQL.
</p>
<p class="fragment" data-fragment-index="4" style="text-align: left;">
  4. <strong>🔑 Configurar la conexión con MySQL</strong>: Ingresa los datos de tu servidor MySQL (nombre de host, puerto, usuario y contraseña). Puedes probar la conexión para asegurarte de que todo esté configurado correctamente.
</p>
<p class="fragment" data-fragment-index="5" style="text-align: left;">
  5. <strong>🖱️ Conectar y empezar a usar</strong>: Haz clic en "OK" para guardar la configuración de la conexión y luego en "Connect". Ahora puedes empezar a usar MySQL Workbench para gestionar tus bases de datos.
</p>


---

#### ⏳ Eventos

Los **eventos** son acciones programadas en MySQL que ocurren automáticamente en intervalos definidos o en un momento específico.

<img src="img/herr_avan/eventos.webp" alt="eventos"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Funciones

Las **funciones** permiten realizar cálculos y transformaciones en los datos de manera modular. Pueden recibir varios argumentos y devuelven un valor **siempre**

<img src="img/herr_avan/funcion.jpeg" alt="funcion"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Procedimientos

Los **procedimientos almacenados** permiten ejecutar un conjunto de instrucciones en MySQL. No devuelven ningún valor.

<img src="img/herr_avan/procedimiento.png" alt="procedimiento"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔁 Triggers

Los **triggers** son acciones automáticas que se ejecutan cuando ocurre un evento en una tabla (como una inserción o actualización). El flujo de un trigger es el siguiente:

<img src="img/herr_avan/trigger.jpg" alt="trigger"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔗 Conclusión

En resumen, estos componentes permiten a MySQL gestionar datos de manera automatizada, modular y eficiente. Utiliza herramientas para mejorar el rendimiento de tus bases de datos. 🚀

<img src="img/herr_avan/conclusion.jpg" alt="conclusion"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

#### 📊 Entendiendo las Vistas

<img src="img/herr_avan/v_1.png" alt="vista 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 Partes de las Vistas

<img src="img/herr_avan/v_2.png" alt="vista 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 Código Ejemplo para una Vista

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