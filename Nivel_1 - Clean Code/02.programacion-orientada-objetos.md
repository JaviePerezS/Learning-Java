# 🧱 Programación Orientada a Objetos (POO)

**POO es un paradigma de programación.**

Un objeto es una entidad, que está conformada por **métodos y atributos**, los atributos de un objeto representan el **estado** de un objeto y los métodos representan el **comportamiento** de dicho objeto.  
Lo que hace que esta estructura sea robusta es la **cohesión**, asegurando que el comportamiento esté directamente vinculado a los atributos que el objeto contiene.

---

## 🧬 Herencia

La **Herencia** es el mecanismo que permite definir una jerarquía de clases donde una **subclase (hija)** hereda el estado y el comportamiento de una **superclase (padre)**.  

Esto promueve la **reutilización de código** y la **especialización**.

Un beneficio clave es la **Sobrescritura de Métodos**, que permite que la clase hija adapte un comportamiento heredado a sus necesidades específicas sin alterar la estructura original.

---

## 🔒 Encapsulamiento

El **encapsulamiento** es el mecanismo que me permite garantizar la integridad del estado.  

Evito que agentes externos manipulen los atributos de forma arbitraria, obligándolos a pasar por métodos que validan las reglas de negocio.

---

## 🔄 El Polimorfismo

El **polimorfismo** permite usar una referencia de una clase padre para trabajar con diferentes clases hijas, pudiendo ejecutar el comportamiento específico de cada una en tiempo de ejecución.  

El polimorfismo aplica el principio **Open/Closed**, ya que permite que el objeto pueda estar **abierto a la extensión**, pero **cerrado a la modificación**, lo cual es ideal al momento de escalar un proceso.

---

### 💳 Ejemplo

En este caso la clase base `MetodoPago` tiene unas características, contiene un método como `procesarPago` el cual tiene el modificador de acceso `abstract` ya que no es fijo sino que dependiendo de la opción que elija el cliente toma dicho valor.

Entonces tenemos las clases hijas las cuales son:

- `PagoTarjeta`
- `PagoNequi`
- `PagoPSE`

Las cuales toman los atributos de `MetodoPago` según el método que el cliente seleccione, haciendo que la clase padre como `procesarPago` pueda continuar agregando diferentes métodos de pago.

Lo que convierte la clase `MetodoPago` en **abierta a la extensión y cerrada a la modificación**, ya que no modifica las clases hijas que ya existen y funcionan como `PagoNequi`, `PagoPSE`, `PagoTarjeta`.

---

## 🎯 Abstracción

La **abstracción** es el principio de la programación orientada a objetos que consiste en mostrar solo las características y comportamientos esenciales de un objeto, ocultando los detalles internos de su implementación.
