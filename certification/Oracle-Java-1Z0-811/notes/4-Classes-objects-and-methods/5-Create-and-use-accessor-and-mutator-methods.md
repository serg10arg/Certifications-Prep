## Cheatsheet: Crear y Usar Métodos Accesores (Getters) y Mutadores (Setters) en Java para el Examen 1Z0-811

Este cheatsheet te guiará en la comprensión y la aplicación de métodos accesores y mutadores en Java, un concepto importante para el examen de certificación 1Z0-811. Estos métodos juegan un papel clave en la encapsulación, uno de los principios fundamentales de la programación orientada a objetos.

### 1. ¿Qué son los Métodos Accesores y Mutadores?

- **Métodos Accesores (Getters):** Son métodos que se usan para **obtener el valor de un campo privado** de una clase. Proporcionan un acceso controlado a los datos, permitiendo a otras partes del código leer la información sin exponer los detalles de implementación.
- **Métodos Mutadores (Setters):** Son métodos que se utilizan para **modificar el valor de un campo privado** de una clase. Permiten modificar los datos de un objeto de forma controlada, aplicando validaciones y lógica de negocio si es necesario.

### 2. ¿Por qué Usar Getters y Setters?

- **Encapsulación:** Ocultan la implementación interna de una clase, protegiendo los datos y permitiendo una mayor flexibilidad en el código.
- **Control de Acceso:** Permiten establecer reglas y validaciones al acceder y modificar los datos de un objeto.
- **Mantenimiento del Código:** Facilita la modificación del código sin afectar a otras partes del programa que usan la clase.

### 3. Convenciones de Nombres

- **Getters:** El nombre del método suele comenzar con "get" seguido del nombre del campo, en formato CamelCase (por ejemplo, `getNombre()`, `getEdad()`).
- **Setters:** El nombre del método suele comenzar con "set" seguido del nombre del campo, en formato CamelCase (por ejemplo, `setNombre(String nombre)`, `setEdad(int edad)`).

### 4. Ejemplo Práctico: Creando Getters y Setters

```java
public class Persona {
    private String nombre; // Campo privado
    private int edad;       // Campo privado

    // Constructor
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Método Accesor (Getter) para el nombre
    public String getNombre() {
        return nombre;
    }

    // Método Mutador (Setter) para el nombre
    public void setNombre(String nuevoNombre) {
        nombre = nuevoNombre;
    }

    // Método Accesor (Getter) para la edad
    public int getEdad() {
        return edad;
    }

    // Método Mutador (Setter) para la edad
    public void setEdad(int nuevaEdad) {
        if (nuevaEdad >= 0) {  // Validación para asegurar una edad válida
            edad = nuevaEdad;
        } else {
            System.out.println("La edad no puede ser negativa.");
        }
    }
}
```

### 5. Usando Getters y Setters

```java
public class PruebaPersona {
    public static void main(String[] args) {
        Persona persona = new Persona("Juan", 30);

        // Usando el Getter para obtener el nombre
        System.out.println("Nombre: " + persona.getNombre());

        // Usando el Setter para modificar el nombre
        persona.setNombre("Pedro");
        System.out.println("Nombre modificado: " + persona.getNombre());

        // Usando el Getter y Setter para la edad
        persona.setEdad(-5); // Intentando establecer una edad inválida
        System.out.println("Edad: " + persona.getEdad()); // La edad no se modificó
    }
}
```

### 6. Puntos Clave para el Examen 1Z0-811

- **Declarar los campos como `private` para la encapsulación.**
- **Crear métodos Getters para proporcionar acceso de solo lectura a los campos privados.**
- **Crear métodos Setters para permitir la modificación controlada de los campos privados.**
- **Usar validaciones dentro de los Setters para asegurar la integridad de los datos.**

**¡Domina el uso de Getters y Setters para escribir código Java bien encapsulado y estar preparado para el examen 1Z0-811!**
