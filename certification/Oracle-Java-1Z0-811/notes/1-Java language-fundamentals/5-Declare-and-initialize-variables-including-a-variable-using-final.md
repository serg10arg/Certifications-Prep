## Cheatsheet: Declaración e Inicialización de Variables en Java para el Examen 1Z0-811

Este cheatsheet te ayudará a comprender la declaración e inicialización de variables en Java, incluyendo el uso de la palabra clave `final`, preparándote para el examen de certificación 1Z0-811.

### 1. Tipos de Datos en Java

Java tiene dos tipos fundamentales de datos:

- **Primitivos:** Representan valores simples como enteros, números de punto flotante, caracteres y booleanos. Los tipos primitivos son los bloques de construcción más básicos de un programa Java.
  - `byte`, `char`, `short`, `int`, `long`: Tipos enteros.
  - `float`, `double`: Tipos de punto flotante.
  - `boolean`: Tipo booleano (verdadero o falso).
- **Referencias:** Apuntan a objetos en memoria.

### 2. Declaración de Variables

Declarar una variable significa reservar espacio en memoria para almacenar un valor de un tipo de dato específico. La sintaxis básica es:

```java
<tipo de dato> <nombre de variable>;
```

**Ejemplos:**

```java
int edad;         // Declara una variable entera llamada 'edad'.
double salario;     // Declara una variable de punto flotante llamada 'salario'.
String nombre;    // Declara una variable de referencia al tipo String llamada 'nombre'.
```

### 3. Inicialización de Variables

Asignar un valor inicial a una variable se llama inicialización. Puedes inicializar una variable en la misma línea que la declaración o después.

**Ejemplos:**

```java
int edad = 25;        // Declaración e inicialización en la misma línea.
double salario;
salario = 3500.50;    // Inicialización después de la declaración.

String nombre = "Juan"; // Inicialización de una variable de referencia.
```

### 4. Variables `final`

Una variable `final` es una **constante cuyo valor no puede cambiar después de su inicialización**. Se declara usando la palabra clave `final`.

**Ejemplos:**

```java
final int NUMERO_MAXIMO = 100; // Constante entera.
final double PI = 3.14159;    // Constante de punto flotante.

final String NOMBRE_EMPRESA = "ACME Corp."; // Constante de tipo String.
```

### 5. Importancia de la Inicialización

- **Java no permite usar variables no inicializadas.** El compilador arrojará un error si intentas acceder a una variable antes de inicializarla.
- **Las variables de instancia y estáticas se inicializan con valores por defecto si no las inicializas explícitamente.**
  - Tipos numéricos: 0 (`int`, `long`, `short`, `byte`), 0.0 (`double`, `float`)
  - `boolean`: `false`
  - Referencias: `null`

### 6. Resumen de la Declaración e Inicialización

1.  **Declara la variable especificando el tipo de dato y el nombre.**
2.  **Inicializa la variable con un valor.** Puedes hacerlo en la misma línea de la declaración o después.
3.  **Utiliza `final` para declarar constantes.**
4.  **Recuerda que las variables no inicializadas no se pueden usar.**

**Ejemplos:**

```java
int contador = 0;                 // Declaración e inicialización de un entero.
final double IMPUESTO = 0.16;    // Declaración de una constante double.
String mensaje = "Hola Mundo";   // Declaración e inicialización de un String.

TestClass obj = new TestClass(); // Declaración e inicialización de una referencia a un objeto.
```

### 7. Reglas Adicionales

- **Puedes declarar e inicializar múltiples variables del mismo tipo en una sola línea.**
  - Ejemplo: `int a = 10, b = 20, c = 30;`
- **No puedes declarar variables de diferentes tipos en una sola línea.**
- **Las variables locales (dentro de un método o bloque) deben ser inicializadas antes de su uso.**
- **Las variables `final` deben ser inicializadas en la declaración o en un constructor.**

**Comprender la declaración e inicialización de variables es fundamental para escribir código Java correcto y eficiente. ¡Estudia este cheatsheet y practica para estar preparado para el examen 1Z0-811!**
