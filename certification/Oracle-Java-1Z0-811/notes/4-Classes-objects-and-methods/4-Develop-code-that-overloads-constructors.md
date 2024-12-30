## Cheatsheet: Sobrecarga de Constructores en Java para el Examen 1Z0-811

Este cheatsheet te ayudará a comprender y aplicar el concepto de sobrecarga de constructores en Java, un tema relevante para el examen de certificación 1Z0-811.

### 1. ¿Qué es Sobrecarga de Constructores?

La sobrecarga de constructores en Java se refiere a la capacidad de definir **múltiples constructores** dentro de una clase, cada uno con una **lista de parámetros diferente**. Esto te da flexibilidad al crear objetos, permitiéndote inicializarlos de diversas maneras.

### 2. ¿Por Qué Sobrecargar Constructores?

- **Flexibilidad en la Inicialización:** Puedes ofrecer diferentes opciones para inicializar los objetos según las necesidades del programa.
- **Código Más Limpio:** Evita la repetición de código al proporcionar constructores específicos para casos comunes.
- **Mejor Legibilidad:** Los constructores con nombres descriptivos aclaran el propósito de cada forma de inicialización.

### 3. Reglas para la Sobrecarga

- **Mismo Nombre:** Todos los constructores deben tener el mismo nombre que la clase.
- **Diferentes Parámetros:** Cada constructor debe tener una lista de parámetros única. Esto puede significar un número diferente de parámetros o tipos de datos distintos.

### 4. Ejemplo Práctico: Sobrecarga de Constructores

```java
public class Libro {
    String titulo;
    String autor;
    int añoPublicacion;

    // Constructor por defecto (sin parámetros)
    public Libro() {
        this.titulo = "Sin título";
        this.autor = "Desconocido";
        this.añoPublicacion = 0;
    }

    // Constructor con título y autor
    public Libro(String titulo, String autor) {
        this(titulo, autor, 0); // Llamada al constructor con 3 parámetros
    }

    // Constructor con título, autor y año de publicación
    public Libro(String titulo, String autor, int añoPublicacion) {
        this.titulo = titulo;
        this.autor = autor;
        this.añoPublicacion = añoPublicacion;
    }
}
```

**Explicación:**

- La clase `Libro` tiene tres constructores diferentes.
- El primer constructor es el constructor por defecto.
- El segundo constructor acepta el título y el autor, utilizando el tercer constructor para establecer el año de publicación en un valor predeterminado.
- El tercer constructor acepta todos los detalles del libro.

### 5. Encadenamiento de Constructores

Observa cómo el segundo constructor utiliza `this(titulo, autor, 0)` para llamar al tercer constructor. Esto se denomina **encadenamiento de constructores** y es una práctica común para evitar la duplicación de código.

### 6. Ejemplo de Uso

```java
public class PruebaLibro {
    public static void main(String[] args) {
        // Usando el constructor por defecto
        Libro libro1 = new Libro();
        System.out.println(libro1.titulo + " por " + libro1.autor + " (" + libro1.añoPublicacion + ")");

        // Usando el constructor con título y autor
        Libro libro2 = new Libro("Don Quijote", "Miguel de Cervantes");
        System.out.println(libro2.titulo + " por " + libro2.autor + " (" + libro2.añoPublicacion + ")");

        // Usando el constructor con todos los parámetros
        Libro libro3 = new Libro("Cien años de soledad", "Gabriel García Márquez", 1967);
        System.out.println(libro3.titulo + " por " + libro3.autor + " (" + libro3.añoPublicacion + ")");
    }
}
```

### 7. Puntos Clave para el Examen 1Z0-811

- **Diferenciación:** Los constructores sobrecargados se distinguen por sus listas de parámetros.
- **Llamada al Constructor:** `this()` se usa para llamar a otro constructor de la misma clase. La llamada debe ser la primera línea del constructor.
- **Compilador:** El compilador selecciona el constructor apropiado basándose en los argumentos utilizados en la creación del objeto.

**¡Dominar la sobrecarga de constructores te permitirá escribir código Java más flexible y eficiente, preparándote mejor para el examen 1Z0-811!**
