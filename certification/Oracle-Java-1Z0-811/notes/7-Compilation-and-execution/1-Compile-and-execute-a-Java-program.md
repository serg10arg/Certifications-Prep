## Cheatsheet: Compilar y Ejecutar un Programa Java para el Examen 1Z0-811

Este cheatsheet te ayudará a entender el proceso de compilación y ejecución de un programa Java, un conocimiento fundamental para el examen de certificación 1Z0-811.

### 1. El Proceso de Desarrollo en Java

El desarrollo de un programa en Java involucra los siguientes pasos:

1.  **Escribir el código fuente:** El código fuente es el conjunto de instrucciones escritas en lenguaje Java que definen la lógica del programa. Se guarda en un archivo con extensión `.java`.
2.  **Compilar el código fuente:** El compilador de Java (`javac`) traduce el código fuente a **bytecode**, un lenguaje intermedio que puede ser ejecutado por la Máquina Virtual de Java (JVM). El resultado de la compilación son archivos con extensión `.class`.
3.  **Ejecutar el bytecode:** La JVM carga los archivos `.class` y ejecuta las instrucciones del bytecode.

### 2. El Entorno de Desarrollo Java (JDK)

El JDK (Java Development Kit) proporciona las herramientas necesarias para desarrollar programas Java. Incluye:

- **Compilador (`javac`):** Convierte el código fuente a bytecode.
- **Lanzador (`java`):** Inicia la JVM para ejecutar el bytecode.
- **JVM (Java Virtual Machine):** Ejecuta el bytecode.
- **Librerías Estándar:** Colección de clases predefinidas que proveen funcionalidades comunes.

### 3. Compilación desde la Línea de Comandos

1.  **Abrir la línea de comandos:** Accede a la interfaz de línea de comandos de tu sistema operativo (cmd en Windows, terminal en Linux/macOS).
2.  **Navegar al directorio del archivo .java:** Utiliza el comando `cd` para acceder a la carpeta donde se encuentra tu archivo de código fuente.
3.  **Compilar el código:** Ejecuta el comando `javac` seguido del nombre del archivo `.java`.
    - Ejemplo: `javac MiPrograma.java`
4.  **Verificar la compilación:** Si la compilación es exitosa, se creará un archivo `.class` con el mismo nombre que el archivo `.java`.

### 4. Ejecución desde la Línea de Comandos

1.  **Lanzar la JVM:** Ejecuta el comando `java` seguido del nombre de la clase que contiene el método `main`. No incluyas la extensión `.class`.
    - Ejemplo: `java MiPrograma`
2.  **Ver la salida:** La salida del programa se mostrará en la línea de comandos.

### 5. El Método `main`

- El método `main` es el **punto de entrada** de un programa Java. Es el método que la JVM busca y ejecuta al iniciar el programa.
- Debe tener la siguiente firma: `public static void main(String[] args)`.

### 6. Manejo de Paquetes y Classpath

- **Paquetes:** Organizan las clases en jerarquías para evitar conflictos de nombres y mejorar la modularidad.
- **Classpath:** Indica a la JVM dónde encontrar las clases necesarias para la ejecución del programa.
- **Opción `-d` en `javac`:** Crea la estructura de directorios del paquete al compilar.
- **Opción `-classpath` (o `-cp`) en `java`:** Define el classpath para la ejecución.

### 7. Ejemplo Completo

**Archivo: MiPrograma.java**

```java
package mipaquete; // Declaración del paquete

public class MiPrograma {

    public static void main(String[] args) {
        System.out.println("¡Hola, Mundo!"); // Imprime un mensaje
    }
}
```

**Compilación:**

```bash
javac -d . mipaquete/MiPrograma.java
```

**Ejecución:**

```bash
java -cp . mipaquete.MiPrograma
```

### 8. Consejos para el Examen 1Z0-811

- **Entender la diferencia entre código fuente y bytecode:** El código fuente es legible por humanos, el bytecode es legible por la JVM.
- **Saber la sintaxis del método `main`:** Es fundamental para que el programa pueda ser ejecutado.
- **Comprender el manejo de paquetes y classpath:** Es importante para la organización del código y la resolución de dependencias.
- **Practicar la compilación y ejecución desde la línea de comandos:** Te familiarizarás con el proceso básico de desarrollo en Java.

**Dominar estos conceptos te dará una base sólida para el desarrollo en Java y te ayudará a tener éxito en el examen de certificación 1Z0-811.**
