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

  En Java, la sentencia `switch` ofrece una forma concisa de ejecutar diferentes bloques de código según el valor de una expresión. Sin embargo, una regla fundamental es que **las etiquetas `case` deben ser constantes en tiempo de compilación**. Esto significa que **el valor de cada etiqueta `case` debe ser conocido por el compilador en el momento de la compilación, y no puede ser una variable cuyo valor se determine en tiempo de ejecución**.

  **Ejemplos:**

  **Código válido:**

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
      default:
          System.out.println("Día inválido");
  }
  ```

  En este caso, las etiquetas `case` son constantes enteras (`1`, `2`, `3`), lo cual es válido.

  **Código inválido:**

  ```java
  int dia = 3;
  String diaSemana = "Miércoles";

  switch (dia) {
      case diaSemana: // Inválido: diaSemana es una variable, no una constante
          System.out.println("Es miércoles");
          break;
      // ...
  }
  ```

  En este caso, la etiqueta `case` usa la variable `diaSemana`, lo cual no está permitido.

  Para corregir el código de la sentencia `switch` en el ejemplo de `diaSemana`, debes usar el valor numérico del día (`dia`) en la expresión `switch` y las etiquetas `case` deben ser los números correspondientes a los días de la semana.

  Aquí está el código corregido:

  ```java
  int dia = 3;
  String diaSemana = "Miércoles";

  switch (dia) {
      case 1:
          diaSemana = "Lunes";
          System.out.println("Es lunes");
          break;
      case 2:
          diaSemana = "Martes";
          System.out.println("Es martes");
          break;
      case 3:
          diaSemana = "Miércoles";
          System.out.println("Es miércoles");
          break;
      // ... casos para los demás días de la semana
      default:
          diaSemana = "Día inválido";
          System.out.println("Día inválido");
  }

  ```

  En este código corregido:

  - La sentencia `switch` evalúa el valor de la variable `dia`, que es un número entero.
  - Las etiquetas `case` son los números del 1 al 7, representando los días de la semana.
  - El bloque de código correspondiente al `case 3` se ejecutará, ya que el valor de `dia` es 3.

  **Recuerda que las etiquetas `case` deben ser constantes en tiempo de compilación**, es decir, valores conocidos por el compilador antes de que el programa se ejecute. En este caso, los números 1, 2, 3, etc. son constantes numéricas válidas.

  En el contexto de la sentencia `switch` en Java, una constante se refiere a un valor cuyo valor se conoce en tiempo de compilación y **no puede cambiar durante la ejecución del programa**.

  Las fuentes mencionan algunos ejemplos de constantes que pueden usarse como etiquetas `case`:

  - **Literales numéricos:** como `10`, `20`, `5`, `1.5`, etc. El compilador conoce el valor exacto de estos literales en el momento de la compilación.
  - **Literales de caracteres:** como `'a'`, `'B'`, `'?'`, etc. Al igual que los literales numéricos, su valor es fijo y conocido en tiempo de compilación.
  - **Literales de cadena:** como `"hola"`, `"mundo"`, etc. El valor de la cadena se define entre comillas dobles y no cambia.
  - **Constantes definidas con `final`:** Puedes declarar variables con la palabra clave `final`, lo que las convierte en constantes. Por ejemplo: `final int MAX_VALOR = 100;`. Una vez que se les asigna un valor, no se pueden modificar.
  - **Expresiones constantes:** Las expresiones que involucran solo constantes también se consideran constantes en tiempo de compilación. Por ejemplo: `"Hola" + "Mundo"`, `2 * 5`, etc.

  **Es importante recordar que las variables cuyo valor se determina en tiempo de ejecución no se consideran constantes y no se pueden usar como etiquetas `case`.**

  Por ejemplo, si tienes una variable `int dia = obtenerDiaDeLaSemana()`, donde `obtenerDiaDeLaSemana()` es una función que devuelve el día actual de la semana, no puedes usar `dia` como etiqueta `case` porque su valor no se conoce hasta que se ejecuta el programa.

  #### Literales numéricos

  ```java
  int numero = 10;
  switch (numero) {
      case 10:
          System.out.println("El número es 10");
          break;
      default:
          System.out.println("El número no es 10");
  }
  ```

  #### Literales de caracteres

  ```java
  char caracter = 'a';
  switch (caracter) {
      case 'a':
          System.out.println("El caracter es 'a'");
          break;
      default:
          System.out.println("El caracter no es 'a'");
  }
  ```

  #### Literales de cadena (a partir de Java 7)

  ```java
  String cadena = "hola";
  switch (cadena) {
      case "hola":
          System.out.println("La cadena es 'hola'");
          break;
      default:
          System.out.println("La cadena no es 'hola'");
  }
  ```

  #### Constantes definidas con final

  ```java
  final int MAX_VALOR = 100;
  int numero = 100;
  switch (numero) {
      case MAX_VALOR:
          System.out.println("El número es el máximo");
          break;
      default:
          System.out.println("El número no es el máximo");
  }
  ```

  #### Expresiones constantes

  ```java
  int numero = 2 * 5;
  switch (numero) {
      case 2 * 5:
          System.out.println("El número es el resultado de 2 * 5");
          break;
      default:
          System.out.println("El número no es el resultado de 2 * 5");
  }
  ```

- **Las etiquetas `case` deben ser únicas**: No puedes tener dos `case` con el mismo valor.
- **No es necesario un orden específico**: Los `case` y el `default` pueden estar en cualquier orden.

### 6. Consejos para el Examen

- **Cuidado con el Fall-through**: Presta atención a la presencia o ausencia de `break`.
- **Conoce los Tipos Válidos**: La expresión en el `switch` debe ser de un tipo permitido.

**Dominar la sentencia `switch` te permitirá escribir código Java más claro y eficiente. ¡Estudia este cheatsheet y practica para tener éxito en el examen 1Z0-811!**
