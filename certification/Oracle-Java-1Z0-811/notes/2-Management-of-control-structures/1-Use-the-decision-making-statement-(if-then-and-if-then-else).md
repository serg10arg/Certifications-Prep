## Cheatsheet: Sentencias de Decisión (if-then e if-then-else) en Java para el Examen 1Z0-811

Este cheatsheet te ayudará a comprender el uso de las sentencias de decisión `if-then` e `if-then-else` en Java, preparándote para el examen de certificación 1Z0-811.

### 1. Sentencia `if-then`

La sentencia `if-then` te permite ejecutar un bloque de código **solo si una condición específica se cumple**.

**Sintaxis:**

```java
if (condición) {
  // Código a ejecutar si la condición es verdadera
}
```

**Ejemplo:**

```java
int edad = 20;

if (edad >= 18) {
  System.out.println("Eres mayor de edad.");
}
```

**Explicación:**

- **`condición`**: Una expresión booleana que se evalúa como `true` o `false`.
- **Bloque de código**: El código entre llaves `{}` se ejecuta **solo si la condición es verdadera**.

### 2. Sentencia `if-then-else`

La sentencia `if-then-else` te permite ejecutar un bloque de código **si una condición se cumple** y otro bloque de código **si la condición no se cumple**.

**Sintaxis:**

```java
if (condición) {
  // Código a ejecutar si la condición es verdadera
} else {
  // Código a ejecutar si la condición es falsa
}
```

**Ejemplo:**

```java
int calificación = 70;

if (calificación >= 60) {
  System.out.println("Aprobado");
} else {
  System.out.println("Reprobado");
}
```

**Explicación:**

- **`condición`**: Una expresión booleana.
- **Primer bloque de código**: Se ejecuta si la condición es `true`.
- **Segundo bloque de código**: Se ejecuta si la condición es `false`.

### 3. Expresiones Booleanas en la Condición

La condición en una sentencia `if` debe ser una **expresión booleana**, que se evalúa como `true` o `false`. Puedes usar operadores de comparación y operadores lógicos para crear expresiones booleanas.

**Ejemplos de operadores de comparación:**

- `==`: Igual a
- `!=`: Diferente de
- `>`: Mayor que
- `<`: Menor que
- `>=`: Mayor o igual que
- `<=`: Menor o igual que

**Ejemplos de operadores lógicos:**

- `&&`: AND (y)
- `||`: OR (o)
- `!`: NOT (no)

### 4. Bloques de Código y Sentencias Simples

- Puedes tener múltiples sentencias dentro de un bloque de código `{}`.
- Si solo tienes una sentencia, las llaves `{}` son opcionales.

**Ejemplo con bloque de código:**

```java
if (edad > 18) {
  System.out.println("Eres mayor de edad.");
  System.out.println("Puedes votar.");
}
```

**Ejemplo con sentencia simple (sin llaves):**

```java
if (edad > 18)
  System.out.println("Eres mayor de edad.");
```

### 5. Anidamiento de Sentencias `if`

Puedes anidar sentencias `if` para crear estructuras de decisión más complejas.

**Ejemplo:**

```java
int edad = 25;
boolean tieneLicencia = true;

if (edad >= 18) {
  if (tieneLicencia) {
    System.out.println("Puedes conducir.");
  } else {
    System.out.println("Eres mayor de edad, pero necesitas una licencia para conducir.");
  }
} else {
  System.out.println("No puedes conducir. Eres menor de edad.");
}
```

### 6. Consejos para el Examen

- #### **Cuidado con la indentación**

  Aunque la indentación no afecta la ejecución del código en Java, una buena indentación mejora la legibilidad y ayuda a evitar errores.

  **Ejemplo:**

  ```java
  public void ifTest(boolean flag) {
    if (flag)
    if (flag)
    System.out.println("True False");
    else
    System.out.println("True True");
    else
    System.out.println("False False");
  }
  ```

  El código tiene una indentación confusa que dificulta la lectura y comprensión. Para analizar este tipo de código, la **estrategia clave es re-indentarlo mentalmente o en un editor de texto simple**, como el Bloc de notas, para reflejar correctamente las asociaciones entre las sentencias `if` y `else`.

  Aquí te explico cómo puedes aplicar esta estrategia paso a paso:

  - **Identifica los bloques `if` y `else`:** El código tiene dos sentencias `if` (1 y 2) y dos sentencias `else` (3 y 4).
  - **Recuerda la regla de asociación:** En Java, una sentencia `else` siempre se asocia con la sentencia `if` más cercana que no tenga un `else` asociado.
  - **Re-indenta el código:** Basándote en la regla de asociación, puedes re-indentar el código para que la estructura sea más clara:

    ```java
    public void ifTest(boolean flag) {
        if (flag) { //1
            if (flag) { //2
                System.out.println("True True");
            } else { // 3
                System.out.println("True False");
            }
        } else { // 4
            System.out.println("False False");
        }
    }
    ```

    - **Analiza el flujo del código:** Ahora puedes leer el código con mayor facilidad:

      - Si `flag` es `true`, se entra al primer bloque `if`.
      - Si `flag` sigue siendo `true`, se imprime "True True".
      - Si `flag` es `false`, se imprime "True False".
      - Si `flag` es `false` desde el principio, se imprime "False False".

      **Esta técnica de re-indentación te ayudará a comprender la lógica del código incluso cuando la indentación original sea confusa. Una vez que hayas re-indentado el código, puedes usar un editor como Netbeans o Eclipse para formatearlo automáticamente y compararlo con tu versión.**

      Recuerda que **las fuentes mencionan que una mala indentación puede llevar a errores lógicos difíciles de detectar**. Por lo tanto, es **fundamental que puedas identificar y corregir la indentación para evitar confusiones y errores.**

- #### **Sentencias vacías**

  Una sentencia vacía (`;`) es válida. Puedes usarla para un bloque `if` que no necesita ejecutar código.

  En programación, una **sentencia vacía** se refiere a una línea de código que **no contiene ninguna instrucción o acción**. Se representa simplemente por un **punto y coma (;)**. Aunque parezca superfluo, **es una sentencia válida en Java** y puede utilizarse en ciertos contextos, como en el caso de un bloque `if` que no requiere ejecutar ningún código.

  Las fuentes explican que:

  - Una sentencia vacía es una sentencia válida en Java.
  - Puedes usar una sentencia vacía para un bloque `if` que no necesita ejecutar código.

    **Ejemplo:**

    ```java
    boolean condicion = false;

    if (condicion) {
        // Este bloque se ejecutaría si la condición fuera verdadera.
    } else {
        ; // Sentencia vacía: no se ejecuta ninguna acción.
    }

    ```

  En este caso, el bloque `else` contiene una sentencia vacía, lo que indica que no se debe realizar ninguna acción si la condición del `if` es falsa.

  **¿Por qué usar una sentencia vacía?**

  Aunque puede parecer redundante, hay situaciones donde una sentencia vacía puede ser útil para mejorar la legibilidad del código:

  - **Claridad de intención:** Indica explícitamente que no se pretende realizar ninguna acción en un bloque de código específico.
  - **Mantener la estructura del código:** Permite conservar la estructura de sentencias `if/else` incluso cuando no se requiere ejecutar código en una de las ramas.

  Es importante destacar que, si bien las sentencias vacías son válidas, **su uso excesivo puede dificultar la legibilidad del código**. En general, es preferible reestructurar el código para evitar la necesidad de sentencias vacías.

- #### **Asignación vs. Comparación**

  Asegúrate de usar el operador de comparación `==` para comparar valores, no el operador de asignación `=`.

  Comprender las sentencias de decisión es fundamental para escribir programas Java que tomen decisiones. Estudia este cheatsheet, practica con ejemplos y estarás mejor preparado para el examen 1Z0-811.\*\*
