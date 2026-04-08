
---

# 📘 Diccionario del Desarrollador: Conceptos Clave

Este documento explica los pilares de la programación y la arquitectura de backend usando como analogía un **Sistema de Certificación**.

---

## 🏗️ 1. Fundamentos de Programación (POO)

### **A. Clase**
Es el **plano o molde** de un objeto. No es el objeto en sí, sino las instrucciones de cómo debe ser.
* **Ejemplo:** La clase `Certificado` define que todo certificado debe tener un ID y una fecha, pero no es un certificado real todavía.

### **B. Atributos**
Son las **características o datos** que definen a la clase. Es lo que la clase "tiene".
* **Ejemplo:** En tu código, `fechaEmision` y `url` son atributos.

### **C. Métodos**
Son las **acciones o comportamientos** que la clase puede realizar. Es lo que la clase "hace".
* **Ejemplo:** `save()`, `update()` o `delete()` son los métodos que definen qué acciones se pueden ejecutar sobre un certificado.
* **Nota sobre `void`:** Un método es `void` cuando ejecuta una acción pero no necesita devolverte ninguna información (como borrar algo).

### **D. Interfaz (El Contrato)**
Es un documento que solo lista **qué** debe hacer un objeto, pero no **cómo**. Obliga a cualquier clase que la implemente a cumplir con esos métodos.
* **Ejemplo:** `CertificadoService` es el contrato que exige que existan métodos para guardar y borrar.



---

## 🏛️ 2. Arquitectura Backend (Spring Boot)

### **E. Entity (El Espejo)**
Una **Entidad** es una clase especial que actúa como un **espejo de la base de datos**. Cada campo en la clase es una columna en una tabla.
* **Concepto clave:** Si tu clase tiene un atributo `id`, la tabla en la base de datos tendrá una columna `id`. Es la representación digital de un registro real.

### **F. Repository (El Puente)**
El **Repositorio** es la pieza que conecta tu código con la base de datos. Es un "puente" que sabe cómo traducir tus órdenes de Java a lenguaje SQL.
* **Cómo funciona:** Gracias a que hereda de `JpaRepository`, no tienes que escribir el código para "Insertar" o "Seleccionar"; el repositorio ya sabe cómo hacerlo automáticamente.

### **G. Service (La Lógica)**
Es donde vive la "inteligencia" del negocio. Aquí es donde decides qué pasa con los datos antes de guardarlos o después de leerlos.
* **Ejemplo:** En `CertificadoServiceImpl`, tú decides que para actualizar primero hay que buscar si el ID existe. Es el intermediario entre el mundo exterior (Controller) y tus datos (Repository).

### **H. Controller (El Portero)**
Es la capa más externa. Su único trabajo es recibir las peticiones del usuario (desde una URL como `/api/certificados`) y pasarle la orden al **Service**.
* **Función:** Valida que la petición sea correcta y entrega la respuesta final al usuario.



---

## 🔄 3. Resumen del Flujo Lógico

1.  El **Controller** recibe la orden del usuario.
2.  El **Service** procesa la lógica y valida los datos.
3.  La **Entity** se usa para dar formato a esos datos.
4.  El **Repository** guarda esa **Entity** en la base de datos real.

---

> **Dato Importante:** Recuerda que la **Interfaz** es lo que permite que el **Controller** no dependa de una clase específica, haciendo que tu sistema sea flexible y fácil de escalar en el futuro.

