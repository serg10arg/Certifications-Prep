## Cheatsheet: Declarar e Inicializar una Variable de Tipo String en Java para el Examen 1Z0-811

Este cheatsheet te ayudará a comprender cómo declarar e inicializar variables de tipo `String` en Java, preparándote para el examen de certificación 1Z0-811.

### 1. ¿Qué es un String en Java?

En Java, un "string" es un **objeto de la clase `java.lang.String`**. Representa una secuencia de caracteres. Cadenas como "1234" o "hola" son en realidad objetos de esta clase. Es importante saber que `String` es una **clase final**, lo que significa que no se puede heredar. Extiende la clase `Object` e implementa la interfaz `java.lang.CharSequence`.

### 2. Declaración de una Variable String

Declarar una variable `String` significa reservar espacio en memoria para almacenar una referencia a un objeto `String`. La sintaxis es la misma que para cualquier otra variable de referencia:

```java
String <nombreVariable>;
```

**Ejemplos:**

```java
String nombre;       // Declara una variable llamada 'nombre' que puede almacenar una referencia a un objeto String.
String apellido;      // Declara una variable llamada 'apellido' de tipo String.
String mensajeError; // Declara una variable llamada 'mensajeError' para almacenar mensajes de error.
```

### 3. Inicialización de una Variable String

Inicializar una variable `String` significa asignarle una referencia a un objeto `String`. Hay varias formas de hacerlo:

#### 3.1. Usando un Literal de String

La forma más común es usar un literal de string, que se escribe entre comillas dobles:

```java
String saludo = "Hola";       // Inicializa la variable 'saludo' con el valor "Hola".
String nombre = "Maria";      // Asigna el valor "Maria" a la variable 'nombre'.
String frase = "Java es genial"; // Inicializa la variable 'frase' con la cadena "Java es genial".
```

#### 3.2. Usando el Constructor de la Clase String

También puedes usar el constructor de la clase `String` para crear un nuevo objeto `String`:

```java
String nombre = new String("Juan"); // Crea un nuevo objeto String con el valor "Juan" y lo asigna a 'nombre'.
```

**Nota:** Aunque esto es válido, es menos eficiente que usar un literal de string. El compilador optimiza los literales de string para evitar la creación de objetos innecesarios.

#### 3.3. Usando Métodos que Devuelven un String

Puedes inicializar una variable `String` con el resultado de un método que devuelve un `String`:

```java
String nombreCompleto = obtenerNombreCompleto(); // 'obtenerNombreCompleto()' es un método que devuelve un String.
```

### 4. Concatenación de Strings

Puedes concatenar strings usando el operador `+`:

```java
String nombre = "Ana";
String apellido = "Perez";
String nombreCompleto = nombre + " " + apellido; // Concatena los strings con un espacio en el medio.
```

### 5. Importancia de la Inmutabilidad

Los objetos `String` en Java son **inmutables**, lo que significa que **no se pueden modificar después de su creación**. Cualquier operación que parezca modificar un `String` en realidad crea un nuevo objeto `String` con el valor modificado.

### 6. Resumen de Declaración e Inicialización

1. **Declara la variable:** `String <nombreVariable>;`
2. **Inicializa la variable:**
   - Usando un literal de string: `String saludo = "Hola";`
   - Usando el constructor `String`: `String nombre = new String("Juan");`
   - Usando un método que devuelve un `String`: `String nombreCompleto = obtenerNombreCompleto();`

### 7. Ejemplos Adicionales

```java
// Declaración e inicialización en una sola línea
String ciudad = "Buenos Aires";

// Inicialización usando un literal de string vacío
String textoVacio = "";

// Concatenación de strings para formar un mensaje
String mensaje = "Hola, " + nombre + ". Bienvenido a " + ciudad + ".";
```

**Comprender la declaración e inicialización de variables `String` es esencial para trabajar con texto en Java. ¡Estudia este cheatsheet y practica para estar preparado para el examen 1Z0-811!**
