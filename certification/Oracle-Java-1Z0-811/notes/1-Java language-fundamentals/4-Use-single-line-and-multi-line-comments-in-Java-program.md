## Cheatsheet: Comentarios en Java para el Examen 1Z0-811

Este cheatsheet te ayudará a comprender cómo usar los comentarios de una línea y multilínea en Java, preparándote para el examen de certificación 1Z0-811.

### 1. ¿Por qué usar comentarios?

Aunque ignorados por el compilador, los comentarios son **cruciales para la legibilidad y el mantenimiento del código**.

- **Explican el código:** Ayudan a comprender la lógica y el propósito del código, especialmente cuando no es evidente.
- **Documentan el código:** Sirven como referencia para otros programadores (¡y para ti mismo en el futuro!) para entender cómo funciona el código.
- **Deshabilitan código temporalmente:** Permiten "desactivar" partes del código sin eliminarlas, lo cual es útil durante la depuración o pruebas.

### 2. Tipos de Comentarios en Java

Java ofrece dos tipos de comentarios:

- **Comentarios de una línea:** Comienzan con `//` y se extienden hasta el final de la línea. Son ideales para comentarios cortos y explicaciones simples.
- **Comentarios multilínea:** Comienzan con `/*` y terminan con `*/`. Permiten escribir comentarios que abarren múltiples líneas, ideales para descripciones más extensas o para deshabilitar bloques de código.

### 3. Ejemplos Prácticos

#### 3.1. Comentarios de una línea

```java
// Este es un comentario de una línea que explica la siguiente línea de código.
int edad = 25; // Declaración e inicialización de la variable 'edad'.
```

#### 3.2. Comentarios multilínea

```java
/*
 * Este es un comentario multilínea que describe la clase 'Persona'.
 * Esta clase contiene información sobre el nombre y la edad de una persona.
 */
public class Persona {
    String nombre;
    int edad;

    /*
     * Constructor de la clase 'Persona' que recibe el nombre y la edad.
     * @param nombre El nombre de la persona.
     * @param edad La edad de la persona.
     */
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

### 4. Comentarios Javadoc

Java ofrece un formato especial de comentarios multilínea llamado **Javadoc**, que se utiliza para generar documentación HTML a partir del código fuente.

- Los comentarios Javadoc comienzan con `/**` y terminan con `*/`.
- Incluyen etiquetas especiales (`@param`, `@return`, `@see`, etc.) para documentar parámetros, valores de retorno, referencias a otras clases y más.

**Ejemplo:**

```java
/**
 * Este método calcula la suma de dos números enteros.
 * @param a El primer número entero.
 * @param b El segundo número entero.
 * @return La suma de a y b.
 */
public int sumar(int a, int b) {
    return a + b;
}
```

### 5. Convenciones y Mejores Prácticas

- **Escribe comentarios claros y concisos:** Evita comentarios redundantes o que simplemente replicen lo que el código ya indica.
- **Mantén los comentarios actualizados:** Si modificas el código, asegúrate de actualizar los comentarios para reflejar los cambios.
- **Utiliza comentarios Javadoc para documentar APIs:** Esto facilita la comprensión y el uso de tu código por parte de otros programadores.
- **No abuses de los comentarios:** Un código bien escrito debe ser autoexplicativo en la mayoría de los casos.

**Recuerda que los comentarios son una herramienta valiosa para mejorar la calidad y la mantenibilidad de tu código. ¡Úsalos con sabiduría!**
