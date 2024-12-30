## Cheatsheet: Formatear Cadenas Usando Secuencias de Escape en Java para el Examen 1Z0-811

Este cheatsheet te ayudará a comprender y usar el formateo de cadenas en Java usando secuencias de escape, un tema importante para el examen de certificación 1Z0-811. Te enfocarás en los especificadores de formato `%d`, `%n` y `%s`, así como en algunas secuencias de escape comunes.

### 1. ¿Qué es el Formateo de Cadenas?

El formateo de cadenas te permite crear cadenas de texto con un formato específico, incluyendo variables y caracteres especiales. En Java, puedes usar el método `System.out.format()` o `String.format()` para formatear cadenas.

### 2. Especificadores de Formato

Los especificadores de formato son marcadores de posición que indican dónde y cómo se deben insertar los valores en la cadena.

- **`%s`**: Inserta una cadena de texto.
- **`%d`**: Inserta un valor numérico entero (int).
- **`%n`**: Inserta un salto de línea.

### 3. Secuencias de Escape

Las secuencias de escape se usan para representar caracteres especiales dentro de una cadena.

- **`\n`**: Salto de línea.
- **`\t`**: Tabulación.
- **`\\`**: Barra invertida.

### 4. Ejemplos Prácticos

**Ejemplo 1: Usando `%s`, `%d` y `%n`**

```java
String nombre = "Juan";
int edad = 30;

System.out.format("Hola, %s!%nTu edad es: %d%n", nombre, edad);
```

**Salida:**

```
Hola, Juan!
Tu edad es: 30
```

**Ejemplo 2: Usando Secuencias de Escape**

```java
String rutaArchivo = "C:\\Archivos\\documento.txt";
System.out.println("La ruta del archivo es: " + rutaArchivo);
```

**Salida:**

```
La ruta del archivo es: C:\Archivos\documento.txt
```

**Ejemplo 3: Formateando una Cadena para Almacenarla**

```java
String mensaje = String.format("Estimado %s, su saldo es %d.", nombre, saldo);
// Puedes guardar 'mensaje' en una base de datos o enviarlo por correo electrónico.
```

### 5. Puntos Importantes para el Examen

- **Número de Argumentos**: El número de especificadores de formato debe coincidir con el número de argumentos que se pasan al método `format()`.
- **Tipo de Datos**: El tipo de dato del argumento debe coincidir con el especificador de formato. Si se usa `%d`, el argumento debe ser un entero.
- **Manejo de Excepciones**: Un error de formato (como pasar una cadena a `%d`) puede lanzar una excepción `IllegalFormatConversionException`.
- **Secuencias de Escape en Literales `char`**: Puedes usar secuencias de escape para definir caracteres especiales en literales `char`. Por ejemplo: `char tab = '\t';`.
- **Uso en `System.out.println()`**: Aunque los ejemplos usan `System.out.format()`, puedes usar secuencias de escape y algunos especificadores de formato directamente en `System.out.println()`.

**¡Practica con estos ejemplos y conceptos para estar bien preparado para el examen 1Z0-811!**
