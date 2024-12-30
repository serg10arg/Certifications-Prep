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

- **Cuidado con la indentación**: Aunque la indentación no afecta la ejecución del código en Java, una buena indentación mejora la legibilidad y ayuda a evitar errores.
- **Sentencias vacías**: Una sentencia vacía (`;`) es válida. Puedes usarla para un bloque `if` que no necesita ejecutar código.
- **Asignación vs. Comparación**: Asegúrate de usar el operador de comparación `==` para comparar valores, no el operador de asignación `=`.

**Comprender las sentencias de decisión es fundamental para escribir programas Java que tomen decisiones. Estudia este cheatsheet, practica con ejemplos y estarás mejor preparado para el examen 1Z0-811.**
