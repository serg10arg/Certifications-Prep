## Cheatsheet: Uso de Operadores Relacionales en Java para el Examen 1Z0-811

Este cheatsheet te guiará en el uso de operadores relacionales en Java, un concepto fundamental para el examen de certificación 1Z0-811. Los operadores relacionales se utilizan para comparar valores y producir un resultado booleano (`true` o `false`).

### 1. Operadores Relacionales en Java

| Operador | Descripción                                                                        | Ejemplo  |
| :------- | :--------------------------------------------------------------------------------- | :------- |
| `==`     | Comprueba si dos valores son iguales.                                              | `a == b` |
| `!=`     | Comprueba si dos valores son diferentes.                                           | `a != b` |
| `>`      | Comprueba si el valor de la izquierda es mayor que el valor de la derecha.         | `a > b`  |
| `<`      | Comprueba si el valor de la izquierda es menor que el valor de la derecha.         | `a < b`  |
| `>=`     | Comprueba si el valor de la izquierda es mayor o igual que el valor de la derecha. | `a >= b` |
| `<=`     | Comprueba si el valor de la izquierda es menor o igual que el valor de la derecha. | `a <= b` |

### 2. Tipos de Datos y Operadores Relacionales

Los operadores relacionales se pueden usar con diversos tipos de datos, incluyendo:

- **Tipos numéricos:** `int`, `long`, `double`, `float`, etc.
- **Caracteres:** `char`
- **Booleanos:** `boolean`

**Es importante recordar que el operador `==` compara valores, mientras que el operador `=` se utiliza para la asignación.**

### 3. Ejemplos Prácticos

**Ejemplo 1: Comparación de enteros**

```java
int a = 10;
int b = 5;

boolean resultado = a > b; // true, porque 10 es mayor que 5
System.out.println("¿a es mayor que b? " + resultado);
```

**Ejemplo 2: Comparación de cadenas**

```java
String cadena1 = "Hola";
String cadena2 = "hola";

boolean resultado = cadena1 == cadena2; // false, las cadenas son sensibles a mayúsculas y minúsculas
System.out.println("¿Las cadenas son iguales? " + resultado);
```

**Ejemplo 3: Comparación de booleanos**

```java
boolean flag1 = true;
boolean flag2 = false;

boolean resultado = flag1 != flag2; // true, los valores booleanos son diferentes
System.out.println("¿Los booleanos son diferentes? " + resultado);
```

### 4. Uso en Estructuras de Control de Flujo

Los operadores relacionales se usan frecuentemente en estructuras de control de flujo como:

- **Sentencias `if`:**

```java
if (edad >= 18) {
  System.out.println("Eres mayor de edad.");
} else {
  System.out.println("Eres menor de edad.");
}
```

- **Bucles `while`:**

```java
int contador = 0;
while (contador < 10) {
  System.out.println("Contador: " + contador);
  contador++;
}
```

### 5. Consideraciones Importantes para el Examen

- **Comparación de Objetos:** Para comparar objetos, se deben utilizar los métodos `equals()` y `compareTo()` en lugar de operadores relacionales como `==` y `!=`.
- **Precedencia de Operadores:** Comprende la precedencia de los operadores para evaluar expresiones complejas correctamente.
- **Conversión de Tipos:** Ten en cuenta la conversión de tipos al comparar valores de diferentes tipos de datos.

**Dominar el uso de operadores relacionales en Java es esencial para escribir código efectivo y comprender los conceptos básicos de programación. ¡Estudia este cheatsheet, practica y estarás bien preparado para el examen 1Z0-811!**
