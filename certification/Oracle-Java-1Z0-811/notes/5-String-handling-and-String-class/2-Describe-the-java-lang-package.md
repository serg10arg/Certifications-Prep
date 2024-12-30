## Cheatsheet: Descripción del Paquete `java.lang` en Java para el Examen 1Z0-811

Este cheatsheet te guiará en la comprensión del paquete `java.lang` en Java, un tema fundamental para el examen de certificación 1Z0-811. El paquete `java.lang` proporciona clases esenciales que forman la base del lenguaje Java. Estas clases están **disponibles automáticamente** en cualquier programa Java sin necesidad de importarlas explícitamente.

### 1. Importancia del Paquete `java.lang`

- **Fundamento del Lenguaje:** Contiene las clases fundamentales que definen los tipos de datos básicos, la gestión de objetos y el manejo de excepciones.
- **Uso Implícito:** Las clases de este paquete se importan automáticamente, lo que significa que puedes usarlas directamente sin la instrucción `import`.
- **Esencial para la JVM:** La Máquina Virtual de Java (JVM) depende en gran medida de las clases del paquete `java.lang` para ejecutar el código Java.

### 2. Clases Clave del Paquete `java.lang`

El paquete `java.lang` contiene una variedad de clases esenciales, pero para el examen 1Z0-811, debes centrarte en las siguientes:

#### **`Object`**

- **Clase Raíz:** Es la clase base de la que heredan todas las demás clases en Java.
- **Métodos Comunes:** Define métodos que son heredados por todas las clases, como `equals()`, `hashCode()`, `toString()`, `getClass()`, `notify()`, `wait()`, etc.
- **Ejemplo:**
  ```java
  Object obj = new String("Ejemplo"); // Cualquier clase hereda de Object
  String str = obj.toString(); // Usando el método toString() de la clase Object
  ```

#### **`String`**

- **Cadenas Inmutables:** Representa una secuencia de caracteres inmutable.
- **Creación de Objetos String:**
  - `String()` - Crea una cadena vacía.
  - `String(String str)` - Crea una copia de la cadena dada.
  - `String(byte[] bytes)` - Crea una cadena a partir de un arreglo de bytes, usando el juego de caracteres predeterminado de la plataforma.
  - `String(char[] value)` - Crea una cadena a partir de un arreglo de caracteres.
- **Métodos Comunes:** `length()`, `charAt()`, `indexOf()`, `substring()`, `toUpperCase()`, `toLowerCase()`, `equals()`, `compareTo()`, `split()`, etc.

#### **`System`**

- **Interacción con el Sistema:** Proporciona acceso a variables y métodos relacionados con el sistema, como la entrada estándar, la salida estándar y el manejo de errores.
- **`System.out`:** Una variable estática de tipo `PrintStream` que representa la salida estándar (consola).
  - **`println()`:** Imprime una línea de texto en la consola.
  - **`print()`:** Imprime texto en la consola sin un salto de línea.
- **Ejemplo:**
  ```java
  System.out.println("¡Hola Mundo!"); // Imprime "¡Hola Mundo!" en la consola
  ```

#### **`Math`**

- **Operaciones Matemáticas:** Ofrece una biblioteca de funciones matemáticas como seno, coseno, raíz cuadrada, valores absolutos, etc.
- **Métodos Estáticos:** Todos los métodos de la clase `Math` son estáticos, lo que significa que se pueden usar directamente sin crear una instancia de la clase.
- **Ejemplos:**
  ```java
  double raizCuadrada = Math.sqrt(25); // raizCuadrada = 5.0
  double numeroAleatorio = Math.random(); // Genera un número aleatorio entre 0.0 y 1.0
  ```

#### **`Wrapper Classes`** (Clases Envoltorio)

- **Encapsulación de Tipos Primitivos:** Proporcionan una forma de representar tipos de datos primitivos como objetos.
- **Clases:** `Integer`, `Double`, `Boolean`, `Character`, `Byte`, `Short`, `Long`, `Float`.
- **Autoboxing y Unboxing:** Conversión automática entre tipos primitivos y sus correspondientes clases envoltorio.
- **Ejemplo:**
  ```java
  int numeroPrimitivo = 10;
  Integer numeroObjeto = Integer.valueOf(numeroPrimitivo); // Autoboxing
  int otroNumero = numeroObjeto.intValue(); // Unboxing
  ```

#### **`Throwable`**

- **Manejo de Excepciones:** Es la clase base para todas las excepciones y errores en Java.
- **Jerarquía de Excepciones:** Define la jerarquía de clases de excepciones, incluyendo `Error` y `Exception`.
- **Métodos:** `getMessage()`, `printStackTrace()`, etc.

### 3. Puntos Clave para el Examen 1Z0-811

- **Importancia de `java.lang`:** Comprender que `java.lang` es un paquete fundamental que proporciona clases esenciales y es accesible automáticamente.
- **Conocimiento de las Clases Clave:** Familiarizarse con las clases clave del paquete `java.lang` y sus métodos más importantes.
- **Diferenciar entre Primitivos y Wrappers:** Entender la diferencia entre tipos de datos primitivos y sus correspondientes clases envoltorio, así como los conceptos de autoboxing y unboxing.

**¡Dominar el paquete `java.lang` es crucial para construir una base sólida en Java y tener éxito en el examen 1Z0-811!**
