## Cheatsheet: Desarrollo de Código con Métodos de la Clase String en Java para el Examen 1Z0-811

Este cheatsheet te guiará en el uso de métodos de la clase `String` en Java, un tema crucial para el examen de certificación 1Z0-811. La clase `String` proporciona una amplia gama de métodos para manipular cadenas de caracteres, un aspecto fundamental en el desarrollo de aplicaciones Java.

### 1. La Clase String en Java

En Java, una **"cadena"** es un objeto de la clase `java.lang.String`. Representa una secuencia de caracteres inmutable, lo que significa que una vez creada, su contenido no puede ser modificado.

La clase `String` ofrece una variedad de métodos para trabajar con cadenas, incluyendo:

- Obtener información sobre la cadena (longitud, caracteres específicos).
- Buscar y manipular subcadenas.
- Convertir la cadena a mayúsculas o minúsculas.
- Comparar cadenas.
- Dividir cadenas en subcadenas.

### 2. Métodos Esenciales de la Clase String

Aquí te presentamos algunos de los métodos más importantes de la clase `String` que debes conocer para el examen 1Z0-811, con ejemplos prácticos y explicaciones:

#### **Obtener información sobre la cadena:**

- **`int length()`**: Devuelve la longitud de la cadena (número de caracteres).

  ```java
  String saludo = "Hola Mundo";
  int longitud = saludo.length(); // longitud = 10
  ```

- **`char charAt(int index)`**: Devuelve el caracter en la posición especificada por el índice (comenzando desde 0).
  ```java
  String palabra = "Java";
  char letra = palabra.charAt(2); // letra = 'v'
  ```

#### **Buscar Subcadenas:**

- **`int indexOf(int ch/String str)`**: Devuelve el índice de la primera aparición del caracter o subcadena especificada. Si no se encuentra, devuelve -1.
  ```java
  String texto = "Este es un ejemplo";
  int indice = texto.indexOf("un"); // indice = 8
  ```
- **`int lastIndexOf(int ch/String str)`**: Devuelve el índice de la última aparición del caracter o subcadena especificada. Si no se encuentra, devuelve -1.
  ```java
  String texto = "Este es un ejemplo";
  int indice = texto.lastIndexOf("e"); // indice = 13
  ```

#### **Manipular Subcadenas:**

- **`String substring(int beginIndex)`**: Devuelve una nueva cadena que es una subcadena de la cadena original, comenzando desde el índice especificado.
  ```java
  String texto = "Programación";
  String subcadena = texto.substring(4); // subcadena = "amación"
  ```
- **`String substring(int beginIndex, int endIndex)`**: Devuelve una nueva cadena que es una subcadena de la cadena original, comenzando desde el índice de inicio (inclusivo) y terminando antes del índice final (exclusivo).
  ```java
  String texto = "Programación";
  String subcadena = texto.substring(0, 4); // subcadena = "Prog"
  ```

#### **Conversión a Mayúsculas y Minúsculas:**

- **`String toUpperCase()`**: Convierte la cadena a mayúsculas.
  ```java
  String texto = "java";
  String mayusculas = texto.toUpperCase(); // mayusculas = "JAVA"
  ```
- **`String toLowerCase()`**: Convierte la cadena a minúsculas.
  ```java
  String texto = "JAVA";
  String minusculas = texto.toLowerCase(); // minusculas = "java"
  ```

#### **Comparación de Cadenas:**

- **`boolean equals(Object obj)`**: Compara la cadena actual con la cadena especificada en el objeto, teniendo en cuenta mayúsculas y minúsculas.
  ```java
  String cadena1 = "Hola";
  String cadena2 = "Hola";
  boolean iguales = cadena1.equals(cadena2); // iguales = true
  ```
- **`boolean equalsIgnoreCase(String str)`**: Compara la cadena actual con la cadena especificada, ignorando las mayúsculas y minúsculas.

  ```java
  String cadena1 = "Hola";
  String cadena2 = "hOLA";
  boolean igualesIgnorandoMayusculas = cadena1.equalsIgnoreCase(cadena2); // igualesIgnorandoMayusculas = true
  ```

- **`int compareTo(String str)`**: Compara la cadena actual con la cadena especificada lexicográficamente. Devuelve 0 si son iguales, un valor negativo si la cadena actual es lexicográficamente menor, y un valor positivo si es mayor.
  ```java
  String cadena1 = "abc";
  String cadena2 = "def";
  int comparacion = cadena1.compareTo(cadena2); // comparacion = -3 (abc es menor que def)
  ```

#### **Dividir Cadenas:**

- **`String[] split(String regex)`**: Divide la cadena en un array de subcadenas utilizando la expresión regular especificada como delimitador.
  ```java
  String texto = "uno,dos,tres";
  String[] partes = texto.split(","); // partes = ["uno", "dos", "tres"]
  ```

### 3. Puntos Clave para el Examen 1Z0-811

- **Inmutabilidad de las Cadenas:** Las cadenas en Java son inmutables. Los métodos de la clase `String` no modifican la cadena original, sino que devuelven una nueva cadena con los cambios aplicados.
- **Manejo de Índices:** Los índices en las cadenas comienzan en 0. Presta atención al manejo de índices para evitar errores como `IndexOutOfBoundsException`.
- **Comparación con `==` vs. `equals()`**: Utiliza `equals()` para comparar el contenido de las cadenas. El operador `==` compara las referencias de los objetos, lo cual puede no ser lo que deseas al comparar cadenas.

**¡Domina los métodos de la clase `String` para manipular cadenas de caracteres de manera efectiva y estar preparado para el examen 1Z0-811!**
