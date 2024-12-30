## Cheatsheet: Convenciones en un Programa Java para el Examen 1Z0-811

Este cheatsheet te ayudará a entender las convenciones importantes que debes seguir al escribir un programa Java, preparándote para el examen de certificación 1Z0-811.

### 1. ¿Por qué son importantes las convenciones?

Las convenciones en programación son como las reglas de etiqueta en la sociedad. No son obligatorias, pero **facilitan la lectura, comprensión y mantenimiento del código**. Seguir las convenciones de Java te permite:

- **Escribir código más legible:** Un código bien formateado y con nombres descriptivos es más fácil de entender para otros programadores (y para ti mismo en el futuro).
- **Evitar errores:** Algunas convenciones, como el uso de mayúsculas y minúsculas, ayudan a prevenir errores de compilación.
- **Integrarte con la comunidad Java:** Al seguir las convenciones, tu código será más familiar para otros programadores Java, lo que facilita la colaboración y el intercambio de código.

### 2. Convenciones de Nombres

#### 2.1. Mayúsculas y Minúsculas:

Java utiliza una convención llamada "Camel Case" para los nombres de variables, métodos y clases.

- **Nombres de Clases:** Comienzan con mayúscula y cada palabra subsiguiente también comienza con mayúscula.
  - Ejemplo: `MiClase`, `CuentaBancaria`, `GestorDeUsuarios`.
- **Nombres de Métodos:** Comienzan con minúscula y cada palabra subsiguiente comienza con mayúscula.
  - Ejemplo: `calcularSaldo()`, `obtenerNombreUsuario()`, `imprimirFactura()`.
- **Nombres de Variables:** Comienzan con minúscula y cada palabra subsiguiente comienza con mayúscula.
  - Ejemplo: `saldoActual`, `nombreUsuario`, `fechaDeNacimiento`.
- **Nombres de Paquetes:** Generalmente se escriben en minúsculas, aunque pueden usar Camel Case con la primera letra en minúscula.
  - Ejemplo: `mipaquete`, `utilidades`, `gestoresDeDatos`.
- **Constantes:** Se escriben en mayúsculas, con palabras separadas por guiones bajos (`_`).
  - Ejemplo: `MAXIMO_INTENTOS`, `VALOR_PREDETERMINADO`, `URL_SERVIDOR`.

#### 2.2. Nombres Descriptivos:

Los nombres deben ser **claros y concisos**, reflejando el propósito del elemento que representan.

- **Evita abreviaturas o acrónimos que no sean ampliamente conocidos.**
- **Usa nombres que indiquen la función o el tipo de dato.**
  - Ejemplo: `edad` en lugar de `e`, `listaDeClientes` en lugar de `ldc`.

### 3. Convenciones de Formato

#### 3.1. Indentación:

- **Utiliza espacios (generalmente 4) para indentar el código dentro de bloques.** Esto mejora la legibilidad y facilita la identificación de la estructura del código.
  ```java
  if (saldo > 0) {
      System.out.println("Saldo positivo");
  } else {
      System.out.println("Saldo negativo");
  }
  ```

#### 3.2. Espacios en blanco:

- **Añade espacios alrededor de los operadores:** `a + b` en lugar de `a+b`.
- **Añade espacios después de las comas y puntos y coma:** `int a, b, c;` en lugar de `inta,b,c;`.
- **Separa las declaraciones de variables con líneas en blanco:**
  ```java
  int edad = 25;

  String nombre = "Juan";
  ```

#### 3.3. Longitud de las líneas:

- **Mantén las líneas de código a una longitud razonable (generalmente 80 caracteres).** Esto facilita la lectura del código en pantallas pequeñas y evita el desplazamiento horizontal excesivo.

#### 3.4. Organización del código:

- **Agrupa las declaraciones de miembros relacionados.**
- **Utiliza líneas en blanco para separar bloques de código con diferentes propósitos.**

### 4. Convenciones Adicionales

- **Comentarios:** Utiliza comentarios para explicar el código que no es evidente. Los comentarios deben ser claros y concisos.
- **Javadoc:** Utiliza comentarios Javadoc para documentar clases y métodos públicos. Javadoc se utiliza para generar documentación HTML.
- **Uso de llaves (`{}`):** Incluso si un bloque de código contiene una sola sentencia, es recomendable usar llaves para mejorar la legibilidad y evitar errores.
- **Manejo de excepciones:** Maneja las excepciones de forma adecuada utilizando bloques `try-catch` y relanzando excepciones cuando sea necesario.

**Recuerda que estas son solo algunas de las convenciones más comunes en Java. Seguir estas convenciones hará que tu código sea más legible, mantenible y profesional, además de ayudarte a prepararte mejor para el examen 1Z0-811.**
