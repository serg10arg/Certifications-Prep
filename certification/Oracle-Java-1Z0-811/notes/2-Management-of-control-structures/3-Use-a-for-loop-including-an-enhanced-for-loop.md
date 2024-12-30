## Cheatsheet: Uso del Bucle For, incluyendo el Bucle For Mejorado (Enhanced For Loop), para el Examen 1Z0-811

Este cheatsheet te guiará en el uso de bucles `for` en Java, incluyendo el bucle `for` mejorado (enhanced for loop), para que te prepares eficazmente para el examen de certificación 1Z0-811.

### 1. Bucle For Tradicional

El bucle `for` tradicional te permite ejecutar un bloque de código repetidamente mientras se cumpla una condición específica. Es ideal para iterar un número determinado de veces.

**Sintaxis:**

```java
for (inicialización; condición; actualización) {
  // Código a ejecutar en cada iteración
}
```

**Explicación:**

- **`inicialización`**: Se ejecuta una sola vez al principio del bucle. Generalmente, se utiliza para declarar e inicializar una variable de control.
- **`condición`**: Una expresión booleana que se evalúa antes de cada iteración. Si la condición es `true`, el bucle se ejecuta. Si es `false`, el bucle termina.
- **`actualización`**: Se ejecuta después de cada iteración. Generalmente, se utiliza para modificar la variable de control.

**Ejemplo:**

```java
// Imprimir los números del 1 al 5
for (int i = 1; i <= 5; i++) {
  System.out.println(i);
}
```

**Salida:**

```
1
2
3
4
5
```

### 2. Bucle For Mejorado (Enhanced For Loop)

El bucle `for` mejorado, también conocido como bucle `for-each`, simplifica la iteración sobre arrays y colecciones. Es ideal cuando necesitas acceder a cada elemento sin preocuparte por el índice.

**Sintaxis:**

```java
for (tipo elemento : arrayOColeccion) {
  // Código a ejecutar para cada elemento
}
```

**Explicación:**

- **`tipo`**: El tipo de dato de los elementos en el array o colección.
- **`elemento`**: Una variable que toma el valor de cada elemento en cada iteración.
- **`arrayOColeccion`**: El array o colección sobre el que se itera.

**Ejemplo con Array:**

```java
String[] nombres = {"Ana", "Juan", "Pedro"};

for (String nombre : nombres) {
  System.out.println("Hola, " + nombre + "!");
}
```

**Ejemplo con ArrayList:**

```java
import java.util.ArrayList;

ArrayList<Integer> numeros = new ArrayList<>();
numeros.add(10);
numeros.add(20);
numeros.add(30);

for (Integer numero : numeros) {
  System.out.println(numero * 2);
}
```

### 3. Consideraciones Importantes

- **Variables de Control**: En un bucle `for` tradicional, la variable de control suele declararse dentro del bucle, lo que limita su alcance al bucle.
- **Iterables**: El bucle `for` mejorado funciona con cualquier objeto que implemente la interfaz `java.lang.Iterable`, como arrays y colecciones.
- **Modificaciones**: El bucle `for` mejorado no proporciona una forma directa de modificar los elementos originales del array o colección. Si necesitas modificar los elementos, debes usar un bucle `for` tradicional con índices.

### 4. Consejos para el Examen

- **Elegir el Bucle Adecuado**: Usa el bucle `for` tradicional cuando necesites controlar el índice o modificar los elementos. Usa el bucle `for` mejorado para una iteración simple y legible.
- **Comportamiento**: Entiende cómo se ejecuta cada tipo de bucle y cómo se manejan las condiciones de salida.
- **Práctica**: Practica con ejemplos para familiarizarte con la sintaxis y el funcionamiento de ambos tipos de bucles `for`.

**Dominar los bucles `for` es esencial para escribir código Java eficaz. ¡Estudia este cheatsheet, practica y estarás bien preparado para el examen 1Z0-811!**
