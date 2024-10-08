## 🌐 MySQL: Vistas, Eventos, Funciones, Procedimientos y Triggers

---

## 📊 Vistas

Las **vistas** son tablas virtuales que permiten visualizar datos sin duplicarlos. A continuación, se muestra el flujo de una vista:

<img src="img/vistas_1.png" alt="vistas_1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

## ⏳ Eventos

Los **eventos** son acciones programadas en MySQL que ocurren automáticamente en intervalos definidos o en un momento específico. Este es el flujo de un evento:

<div class="mermaid">
graph TD
    A[Evento Programado] -->|Tiempo| B[Acción Automática]
    B --> C[Tarea Completada]
</div>

---

## 🛠️ Funciones

Las **funciones** permiten realizar cálculos y transformaciones en los datos de manera modular. El flujo típico de una función es el siguiente:

<div class="mermaid">
graph TD
    A[Entrada de Datos] -->|Llama a Función| B[Función MySQL]
    B -->|Devuelve Resultado| C[Salida de Datos]
</div>

---

## 🌀 Procedimientos

Los **procedimientos almacenados** permiten ejecutar un conjunto de instrucciones en MySQL. Este es el flujo de un procedimiento:

<div class="mermaid">
graph TD
    A[Invoca Procedimiento] --> B[Ejecuta Conjunto de Instrucciones]
    B --> C[Resultado del Procedimiento]
</div>

---

## 🔁 Triggers

Los **triggers** son acciones automáticas que se ejecutan cuando ocurre un evento en una tabla (como una inserción o actualización). El flujo de un trigger es el siguiente:

<div class="mermaid">
graph TD
    A[Cambio en Tabla] -->|Acción| B[Dispara Trigger]
    B -->|Ejecuta| C[Acción Automática]
</div>

---

## 🔗 Conclusión

En resumen, estos componentes permiten a MySQL gestionar datos de manera automatizada, modular y eficiente. Utiliza estos gráficos para entender cómo interactúan y mejorar el rendimiento de tus bases de datos. 🚀

---


