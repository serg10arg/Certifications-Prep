## Cheatsheet: Manejo de Excepciones Comunes en Java para el Examen 1Z0-811

Este cheatsheet te ayudará a entender cómo manejar las excepciones comunes que se lanzan en Java, un tema crucial para el examen de certificación 1Z0-811. La capacidad de manejar excepciones eficazmente es esencial para escribir código Java robusto y confiable.

### 1. ¿Qué son las Excepciones?

Las **excepciones** son eventos inesperados que ocurren durante la ejecución de un programa y que interrumpen el flujo normal del código. Pueden ser causadas por errores del programador, errores de entrada del usuario, problemas de hardware, entre otros factores.

### 2. Tipos de Excepciones

En Java, las excepciones se clasifican en dos categorías principales:

- **Excepciones Verificadas (Checked Exceptions):** El compilador te obliga a manejar estas excepciones, ya sea capturándolas con un bloque `try-catch` o declarándolas en la cláusula `throws` del método.
  - Ejemplos: `IOException`, `SQLException`, `ClassNotFoundException`.
- **Excepciones No Verificadas (Unchecked Exceptions):** El compilador no te obliga a manejar estas excepciones.
  - Suelen ser causadas por errores de lógica en el código.
  - Ejemplos: `NullPointerException`, `ArrayIndexOutOfBoundsException`, `ArithmeticException`.

### 3. Manejo de Excepciones con `try-catch`

El bloque `try-catch` es la forma más común de manejar excepciones en Java. Permite capturar una excepción y ejecutar un código específico para manejarla, evitando que el programa se detenga abruptamente.

**Sintaxis:**

```java
try {
    // Código que puede lanzar una excepción
} catch (TipoDeExcepcion e) {
    // Código para manejar la excepción
}
```

**Ejemplo:**

```java
try {
    int resultado = 10 / 0; // División por cero
} catch (ArithmeticException e) {
    System.out.println("Error: División por cero.");
}
```

### 4. Cláusula `finally`

La cláusula `finally` se usa para ejecutar un código **siempre**, independientemente de si se lanza o no una excepción. Es útil para liberar recursos como archivos o conexiones de bases de datos.

**Ejemplo:**

```java
try {
    // Abrir un archivo
    // Leer datos del archivo
} catch (IOException e) {
    System.out.println("Error al leer el archivo.");
} finally {
    // Cerrar el archivo
}
```

### 5. Excepciones Comunes y sus Causas

Aquí hay algunas de las excepciones más comunes que se lanzan en Java y sus causas:

- **`NullPointerException`:** Se lanza cuando se intenta acceder a un miembro de un objeto que es `null`.
  - **Ejemplo:** `String str = null; int longitud = str.length();`
- **`ArrayIndexOutOfBoundsException`:** Se lanza cuando se intenta acceder a un elemento de un array con un índice inválido (fuera de los límites del array).
  - **Ejemplo:** `int[] array = {1, 2, 3}; int elemento = array;`
- **`ArithmeticException`:** Se lanza cuando se produce un error aritmético, como la división por cero.
  - **Ejemplo:** `int resultado = 10 / 0;`
- **`ClassCastException`:** Se lanza cuando se intenta convertir un objeto a un tipo incompatible.
- **`IllegalArgumentException`:** Se lanza cuando se pasa un argumento inválido a un método.
  - **Ejemplo:** Un método que espera un número positivo como argumento y se le pasa un número negativo.
- **`IOException`:** Se lanza cuando ocurre un error de entrada/salida, como al leer o escribir un archivo.
- **`StringIndexOutOfBoundsException`:** Se lanza al intentar acceder a un carácter en un `String` con un índice inválido.
  - **Ejemplo:** `String str = "Hola"; char caracter = str.charAt(5);`

### 6. Consejos para el Examen 1Z0-811

- **Conocer la jerarquía de excepciones:** Familiarízate con las diferentes clases de excepciones y sus relaciones.
- **Comprender la diferencia entre excepciones verificadas y no verificadas:** Saber cuándo se requiere manejar una excepción y cuándo no.
- **Practicar el manejo de excepciones con `try-catch` y `finally`:** Escribe código que lance y capture diferentes tipos de excepciones.

**¡Dominar el manejo de excepciones es esencial para convertirte en un programador Java competente y tener éxito en el examen 1Z0-811!**
