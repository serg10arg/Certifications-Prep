## Cheatsheet: El Modificador `private` en Java para el Examen 1Z0-811

Este cheatsheet te guiará en la comprensión y el uso del modificador de acceso `private` en Java, un concepto clave para el examen de certificación 1Z0-811. El modificador `private` es fundamental para la encapsulación, uno de los pilares de la programación orientada a objetos.

### 1. ¿Qué son los Modificadores de Acceso?

En Java, los modificadores de acceso controlan la visibilidad y el acceso a los miembros de una clase (campos, métodos y constructores). Permiten al desarrollador definir qué partes de una clase pueden ser accedidas desde otras partes del código.

### 2. El Modificador `private`

El modificador `private` es el más restrictivo de los modificadores de acceso en Java. Un miembro declarado como `private` **solo puede ser accedido desde dentro de la misma clase** en la que está definido.

### 3. Beneficios de Usar `private`

- **Encapsulación:** Oculta los detalles de implementación interna de una clase, protegiéndolos de accesos externos no deseados.
- **Control de Acceso:** Permite un control preciso sobre cómo se modifican los datos de un objeto.
- **Mantenimiento del Código:** Facilita la modificación del código sin afectar a otras partes del programa que usan la clase.

### 4. Ejemplo Práctico

```java
public class CuentaBancaria {
    private double saldo; // El saldo es privado y solo accesible desde la clase

    public CuentaBancaria(double saldoInicial) {
        this.saldo = saldoInicial;
    }

    public double obtenerSaldo() { // Método público para acceder al saldo
        return saldo;
    }

    public void depositar(double cantidad) { // Método público para modificar el saldo
        saldo += cantidad;
    }
}
```

En este ejemplo:

- El campo `saldo` es `private`. No puede ser accedido directamente desde fuera de la clase `CuentaBancaria`.
- Los métodos `obtenerSaldo()` y `depositar()` son `public`. Permiten un acceso controlado al saldo desde otras partes del código.

### 5. `private` y Encapsulación

El uso de `private` es esencial para lograr la encapsulación. Al declarar los campos como `private` y proporcionar métodos públicos para acceder y modificarlos (getters y setters), se protege la integridad de los datos y se mejora la flexibilidad del código.

### 6. Puntos Clave para el Examen 1Z0-811

- **Alcance de `private`:** Un miembro `private` solo es accesible dentro de la misma clase.
- **Encapsulación:** El uso de `private` es fundamental para la encapsulación.
- **Métodos Getters y Setters:** Se usan para proporcionar un acceso controlado a los campos `private`.
- **Implicaciones en la Herencia:** Los miembros `private` no son heredados por las subclases.

**¡Domina el uso del modificador `private` para escribir código Java bien encapsulado y estar preparado para el examen 1Z0-811!**
