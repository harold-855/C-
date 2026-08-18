[Anterior ⬅️](../02-Control-de-flujo/04-Switch.md) | [Inicio 🏠](/README.md) | [Siguiente ➡️](./02-metodos-array.md)

# ➡️ Array

### Almacenando múltiples datos de un mismo tipo

Un array es una estructura que te permite almacenar múltiples valores del mismo tipo, accesibles a través de un índice. En C#, los arrays tienen un tamaño fijo, lo que significa que una vez definido el número de elementos, no puede cambiarse. (Arrays, 2023)

También, se conocen como arreglos, porque son una estructura de datos fundamental en la programación, que permite almacenar y gestionar varios elementos de un mismo tipo de datos. Estos elementos se organizan de manera secuencial, con cada uno ocupando una posición dentro del array, lo que facilita su acceso y manipulación.

Los arrays, son especialmente útiles cuando se trabaja con conjuntos de datos relacionados, como listas de nombres, calificaciones de estudiantes, valores de mediciones, entre otros.

---



### 🔎 Sintaxis básica:

```csharp
int[] numbers = new int[5];
numbers[0] = 10;
```


int[] numbers: Declara una variable llamada numbers que contendrá un arreglo de enteros.

new int[5]: Reserva espacio en memoria para almacenar 5 números enteros. C# inicializa automáticamente las 5 casillas con el valor por defecto (0).

numbers[0] = 10;: Asigna el valor 10 a la primera casilla. Como los índices empiezan en 0, las posiciones válidas son de 0 a 4.

---

### 💻 Almacenando múltiples datos de un mismo tipo:

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
```

Permite definir el arreglo y asignar todos sus valores iniciales al mismo tiempo.

El compilador deduce automáticamente el tamaño del arreglo contando los elementos entre las llaves { } (en este caso, tamaño 5).

---

Una de las principales ventajas de los arrays es su capacidad para agrupar y organizar información de manera eficiente, lo que resulta esencial en una amplia variedad de aplicaciones informáticas, desde el procesamiento de datos hasta la implementación de algoritmos complejos.

**Nota:** Los arrays en .NET cuentan con propiedades y métodos específicos que facilitan su manejo. Si deseas profundizar cada uno de ellos, te invitamos a visitar nuestro repositorio oficial en GitHub.

### 📊 Estructura de posiciones en memoria

| Índice (Posición) | Valor almacenado |
| :---: | :---: |
| `numbers[0]` | `10` |
| `numbers[1]` | `20` |
| `numbers[2]` | `30` |
| `numbers[3]` | `40` |
| `numbers[4]` | `50` |