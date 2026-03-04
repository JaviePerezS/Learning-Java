# 🧱 Principios SOLID

Los principios **SOLID** son 5 reglas que nos ayudan a escribir código más limpio, mantenible y escalable.  
Fueron pensados para mejorar el diseño en la Programación Orientada a Objetos.

---

## 🟢 S — Single Responsibility Principle (Responsabilidad Única)

Una clase debe tener **una sola responsabilidad**, es decir, una sola razón para cambiar.

Si una clase hace demasiadas cosas:
- Se vuelve difícil de mantener.
- Se vuelve difícil de probar.
- Se vuelve más propensa a errores.

Cada clase debe encargarse de una única tarea bien definida.

---

## 🔵 O — Open/Closed Principle (Abierto/Cerrado)

Una clase debe estar:

- ✅ Abierta a la extensión  
- ❌ Cerrada a la modificación  

Esto significa que podemos agregar nuevas funcionalidades sin modificar el código que ya funciona.

Se logra comúnmente usando:
- Herencia
- Polimorfismo
- Interfaces

---

## 🟡 L — Liskov Substitution Principle (Sustitución de Liskov)

Una clase hija debe poder sustituir a su clase padre sin alterar el comportamiento esperado del programa.

Si una clase hereda de otra:
- Debe respetar su comportamiento.
- No debe romper la lógica existente.

En otras palabras, si algo funciona con la clase padre, también debe funcionar con la clase hija.

---

## 🟠 I — Interface Segregation Principle (Segregación de Interfaces)

Es mejor tener varias interfaces pequeñas y específicas que una sola interfaz grande y general.

Una clase no debería estar obligada a implementar métodos que no necesita.

Esto evita:
- Código innecesario.
- Métodos vacíos.
- Dependencias forzadas.

---

## 🔴 D — Dependency Inversion Principle (Inversión de Dependencias)

Las clases no deben depender de implementaciones concretas, sino de abstracciones.

Es decir:
- No depender directamente de clases específicas.
- Depender de interfaces o clases abstractas.

Esto hace que el sistema sea:
- Más flexible.
- Más fácil de probar.
- Más sencillo de escalar.

---

