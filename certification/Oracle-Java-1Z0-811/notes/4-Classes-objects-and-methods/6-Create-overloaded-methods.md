## Cheatsheet: Crear Métodos Sobrecargados en Java para el Examen 1Z0-811

Este cheatsheet te guiará en la creación y el uso de métodos sobrecargados en Java, un concepto esencial para el examen de certificación 1Z0-811. La sobrecarga de métodos te permite definir múltiples métodos con el mismo nombre pero con diferentes parámetros dentro de la misma clase.

### 1. ¿Qué es la Sobrecarga de Métodos?

La sobrecarga de métodos es una característica de Java que permite definir **múltiples métodos con el mismo nombre** dentro de una clase, siempre que estos métodos tengan **diferentes listas de parámetros**. Esto significa que pueden diferir en el **número** de parámetros, los **tipos de datos** de los parámetros, o el **orden** de los tipos de datos.

### 2. Beneficios de la Sobrecarga de Métodos

- **Flexibilidad:** Proporciona diferentes maneras de realizar una misma operación, adaptándose a diversos tipos de datos o número de argumentos.
- **Legibilidad:** Permite usar nombres de métodos más intuitivos y descriptivos, haciendo el código más fácil de entender y mantener.
- **Reutilización de Código:** Evita la duplicación de código al permitir que un solo nombre de método maneje diferentes escenarios.

### 3. Reglas de la Sobrecarga de Métodos

- **Mismo Nombre:** Todos los métodos sobrecargados deben tener el mismo nombre.
- **Diferentes Listas de Parámetros:** Los métodos deben diferir en el número, tipos de datos u orden de los parámetros.
- **El Tipo de Retorno No Importa:** El tipo de retorno del método no influye en la sobrecarga. Dos métodos con el mismo nombre y parámetros pero diferentes tipos de retorno no se consideran sobrecargados y generarán un error de compilación.

### 4. Ejemplo Práctico: Sobrecarga de Métodos

```java
public class Calculadora {

    // Método para sumar dos enteros
    public int sumar(int a, int b) {
        return a + b;
    }

    // Método para sumar dos números de punto flotante
    public double sumar(double a, double b) {
        return a + b;
    }

    // Método para sumar tres enteros
    public int sumar(int a, int b, int c) {
        return a + b + c;
    }
}
```

**Explicación:**

- La clase `Calculadora` tiene tres métodos llamados `sumar`, cada uno con diferentes listas de parámetros.
- El primer método suma dos enteros (`int`).
- El segundo método suma dos números de punto flotante (`double`).
- El tercer método suma tres enteros (`int`).

### 5. Uso de Métodos Sobrecargados

```java
public class PruebaCalculadora {
    public static void main(String[] args) {
        Calculadora calc = new Calculadora();

        int sumaEnteros = calc.sumar(5, 10);
        System.out.println("Suma de enteros: " + sumaEnteros); // Imprime 15

        double sumaDoubles = calc.sumar(3.14, 2.71);
        System.out.println("Suma de doubles: " + sumaDoubles); // Imprime 5.85

        int sumaTresEnteros = calc.sumar(1, 2, 3);
        System.out.println("Suma de tres enteros: " + sumaTresEnteros); // Imprime 6
    }
}
```

**Explicación:**

- El compilador de Java selecciona automáticamente el método `sumar` apropiado según los tipos y el número de argumentos utilizados en la llamada.

### 6. Puntos Clave para el Examen 1Z0-811

- **Comprensión de la Firma del Método:** La firma del método incluye el nombre del método y la lista de parámetros. El compilador utiliza la firma para identificar el método correcto a llamar.
- **Resolución de Sobrecarga:** El compilador selecciona el método más específico que coincida con los argumentos proporcionados.
- **Importancia de los Tipos de Datos:** La sobrecarga se basa en la diferencia en los tipos de datos de los parámetros.

**¡Dominar la sobrecarga de métodos te permitirá escribir código Java más flexible, legible y eficiente, preparándote para el éxito en el examen 1Z0-811!**
