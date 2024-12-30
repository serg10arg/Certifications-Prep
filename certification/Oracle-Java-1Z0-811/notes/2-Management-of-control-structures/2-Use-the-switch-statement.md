## Cheatsheet: Uso de la Sentencia Switch en Java para el Examen 1Z0-811

Este cheatsheet te guiará en el uso de la sentencia `switch` en Java, una herramienta poderosa para controlar el flujo de tu programa, preparándote para el examen de certificación 1Z0-811.

### 1. ¿Qué es la Sentencia Switch?

La sentencia `switch` te permite **seleccionar un bloque de código para ejecutar en base al valor de una expresión**. Es una alternativa más legible y eficiente a múltiples sentencias `if-else` cuando se trata de comparar una variable con varios valores constantes.

### 2. Sintaxis de la Sentencia Switch

```java
switch (expresión) {
  case valor1:
    // Código a ejecutar si la expresión es igual a valor1
    break;
  case valor2:
    // Código a ejecutar si la expresión es igual a valor2
    break;
  ...
  default:
    // Código a ejecutar si ningún caso coincide
}
```

**Explicación:**

- **`expresión`**: La expresión que se evalúa. Puede ser de tipo `byte`, `short`, `char`, `int` (y sus wrappers), `enum` o `String`.
- **`case valorX`**: Cada `case` compara la expresión con un valor constante específico.
- **`break`**: La sentencia `break` es **opcional** pero **altamente recomendada**. Indica que la ejecución debe salir del bloque `switch` después de ejecutar el código del `case` coincidente.
- **`default`**: El bloque `default` es **opcional**. Se ejecuta si ningún `case` coincide con la expresión.

### 3. Funcionamiento de la Sentencia Switch

1.  **Evaluación de la Expresión**: Se evalúa la expresión dentro del `switch`.
2.  **Comparación con los `case`**: La expresión se compara con cada valor especificado en los `case`.
3.  **Ejecución del Código**: Si la expresión coincide con un valor `case`, el código asociado a ese `case` se ejecuta.
4.  **Salida del Switch**:
    - Si se encuentra un `break`, la ejecución sale del `switch`.
    - Si no hay `break`, la ejecución continúa en el siguiente `case`, incluso si no coincide (**comportamiento de caída o fall-through**).

### 4. Ejemplo Práctico

```java
int dia = 3;

switch (dia) {
  case 1:
    System.out.println("Lunes");
    break;
  case 2:
    System.out.println("Martes");
    break;
  case 3:
    System.out.println("Miércoles");
    break;
  case 4:
    System.out.println("Jueves");
    break;
  case 5:
    System.out.println("Viernes");
    break;
  default:
    System.out.println("Fin de semana");
}
```

**Salida:** Miércoles

**Explicación:** La variable `dia` tiene el valor 3, por lo que el código asociado al `case 3` se ejecuta. El `break` impide que la ejecución continúe en los siguientes `case`.

### 5. Consideraciones Importantes

- **Las etiquetas `case` deben ser constantes**: No puedes usar variables en las etiquetas `case`.
- **Las etiquetas `case` deben ser únicas**: No puedes tener dos `case` con el mismo valor.
- **No es necesario un orden específico**: Los `case` y el `default` pueden estar en cualquier orden.

### 6. Consejos para el Examen

- **Cuidado con el Fall-through**: Presta atención a la presencia o ausencia de `break`.
- **Conoce los Tipos Válidos**: La expresión en el `switch` debe ser de un tipo permitido.

**Dominar la sentencia `switch` te permitirá escribir código Java más claro y eficiente. ¡Estudia este cheatsheet y practica para tener éxito en el examen 1Z0-811!**
