## Cheatsheet: Uso del Constructor por Defecto con y sin Parámetros en Java para el Examen 1Z0-811

Este cheatsheet se centra en la comprensión y el uso del constructor por defecto en Java, un tema fundamental para el examen de certificación 1Z0-811. Abordaremos la distinción entre constructores con y sin parámetros, cuándo se proporciona el constructor por defecto y cómo usarlo en tus programas Java.

### 1. ¿Qué es un Constructor?

Un constructor es un método especial dentro de una clase que se utiliza para **crear e inicializar nuevos objetos** de esa clase. Se llama automáticamente cuando se usa la palabra clave `new` para crear un objeto.

### 2. Constructor por Defecto

El constructor por defecto es un constructor sin parámetros. **Si no defines ningún constructor explícitamente en una clase, el compilador de Java proporcionará automáticamente un constructor por defecto**. Este constructor no tiene código en su cuerpo, por lo que simplemente crea un objeto con los valores predeterminados para sus campos.

**Ejemplo:**

```java
public class Persona {
    String nombre;
    int edad;

    // No hay constructor definido, por lo que el compilador
    // proporcionará un constructor por defecto:
    // Persona() { }
}
```

### 3. Constructor con Parámetros

Un constructor con parámetros te permite **inicializar los campos de un objeto con valores específicos** en el momento de la creación. Puedes definir tantos constructores con parámetros como necesites, siempre y cuando tengan diferentes listas de parámetros (sobrecarga de constructores).

**Ejemplo:**

```java
public class Persona {
    String nombre;
    int edad;

    // Constructor con parámetros
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

### 4. Cuándo se Proporciona el Constructor por Defecto

El compilador de Java solo proporciona el constructor por defecto **si no hay otros constructores definidos** en la clase. Si defines al menos un constructor (con o sin parámetros), el constructor por defecto ya no se proporciona automáticamente.

### 5. Ejemplo Práctico: Usando Constructores

```java
public class EjemploConstructor {
    public static void main(String[] args) {
        // Usando el constructor por defecto (proporcionado por el compilador)
        Persona persona1 = new Persona();
        System.out.println(persona1.nombre + " " + persona1.edad); // Salida: null 0

        // Usando el constructor con parámetros
        Persona persona2 = new Persona("Ana", 25);
        System.out.println(persona2.nombre + " " + persona2.edad); // Salida: Ana 25
    }
}
```

### 6. Puntos Clave para el Examen 1Z0-811

- **El constructor por defecto se proporciona solo si no se define ningún otro constructor.**
- **Puedes definir múltiples constructores con diferentes parámetros.**
- **Un constructor no tiene tipo de retorno, ni siquiera `void`.**
- **La palabra clave `this` se utiliza para referenciar los campos de la clase dentro del constructor.**

**¡Comprender el uso de constructores con y sin parámetros es crucial para escribir código orientado a objetos en Java y para tener éxito en el examen 1Z0-811!**
