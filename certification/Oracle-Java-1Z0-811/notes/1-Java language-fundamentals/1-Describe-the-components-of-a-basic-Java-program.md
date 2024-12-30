## Cheatsheet: Componentes de un Programa Java Básico para el Examen 1Z0-811

Este cheatsheet te guiará a través de los componentes esenciales de un programa Java básico, preparándote para el examen de certificación 1Z0-811.

### 1. Anatomía de un Archivo Fuente Java

Un archivo fuente Java, con extensión `.java`, contiene el código fuente de tu programa. Su estructura básica se compone de:

- **Sentencia `package` (opcional):** Define el paquete al que pertenece la clase. Debe ser la primera sentencia del archivo.

  ```java
  package mipaquete;
  ```

- **Sentencias `import` (opcional):** Permiten usar clases de otros paquetes sin necesidad de usar sus nombres completos.

  ```java
  import java.util.ArrayList;
  ```

- **Declaraciones de Tipos:** Definen clases, interfaces o enums. Un archivo fuente suele contener una clase pública.

  ```java
  public class MiClase {
      // Cuerpo de la clase
  }
  ```

### 2. Componentes Fundamentales de un Programa Java

- **Clases:** Plantillas para crear objetos. Definen atributos (datos) y métodos (comportamientos).

  ```java
  public class Auto {
      // Atributos
      String marca;
      String modelo;
      int año;

      // Métodos
      void acelerar() {
          // Código para acelerar
      }
  }
  ```

- **Objetos:** Instancias de una clase. Representan entidades concretas con valores específicos para sus atributos.

  ```java
  Auto miAuto = new Auto();
  miAuto.marca = "Toyota";
  miAuto.modelo = "Corolla";
  miAuto.año = 2022;
  ```

- **Métodos:** Bloques de código que definen acciones o comportamientos. Se invocan usando el operador punto (`.`).

  ```java
  miAuto.acelerar();
  ```

### 3. El Método `main`

- Punto de entrada de la ejecución del programa. La JVM busca y ejecuta este método.
- Debe tener una firma específica:

  ```java
  public static void main(String[] args) {
      // Código a ejecutar
  }
  ```

### 4. Comentarios

- **Comentarios de una línea:** `// Comentario`
- **Comentarios multi-línea:** `/* Comentario */`
- **Comentarios Javadoc:** `/** Documentación */` (se usan para generar documentación HTML)

### 5. Compilación y Ejecución

- **Compilación:** Se usa el compilador `javac` para convertir el código fuente `.java` en bytecode `.class`.
- **Ejecución:** Se usa el comando `java` para ejecutar el bytecode. La JVM interpreta el bytecode y lo ejecuta en la máquina.

  **Ejemplo:**

  ```bash
  javac MiPrograma.java
  java MiPrograma
  ```

### 6. El Paquete `java.lang`

- Contiene clases esenciales para la programación en Java, como `Object`, `String`, `System`, `Math` y las clases envoltorio (`Integer`, `Double`, etc.).
- No es necesario importarlo explícitamente.

### 7. La Clase `java.lang.Object`

- Clase raíz de la jerarquía de clases de Java.
- Todos los objetos heredan los métodos de `Object`, como `toString()`, `equals()` y `hashCode()`.

### 8. La Clase `java.lang.System`

- Proporciona acceso a variables de entorno del sistema y flujos de entrada/salida estándar como `System.out` (salida estándar) y `System.err` (salida de error).

### 9. Relación entre Objetos y sus Miembros

- **Un objeto es una instancia de una clase.** Piensa en la clase como un molde y en el objeto como la figura que se crea a partir de ese molde.
- **Los miembros de un objeto son sus variables y métodos.**

### 10. Variables de Clase, Instancia y Locales

- **Variables de clase (`static`):** Pertenecen a la clase en sí, no a las instancias. Se comparten entre todos los objetos de la clase.
- **Variables de instancia:** Pertenecen a cada objeto individual de la clase. Cada objeto tiene su propia copia.
- **Variables locales:** Declaradas dentro de un método o bloque de código. Sólo existen dentro de ese ámbito.

**Recuerda:** Dominar estos conceptos básicos es esencial para escribir programas Java y tener éxito en el examen de certificación 1Z0-811.
