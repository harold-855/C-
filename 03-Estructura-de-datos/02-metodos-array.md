```markdown
# Métodos y Propiedades de los Arrays en C#

## Propiedades

### Length
La propiedad `Length` obtiene el número total de elementos en todas las dimensiones del array.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int length = numbers.Length; // length = 5

```

### Rank

La propiedad `Rank` obtiene el número de dimensiones (o rango) del array.

```csharp
int[,] matrix = new int[3, 5];
int rank = matrix.Rank; // rank = 2

```

---

## Métodos

### GetValue y SetValue

El método `GetValue` obtiene el valor de una posición específica en el array y el método `SetValue` asigna un valor en una posición específica.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int value = (int) numbers.GetValue(2); // value = 30
numbers.SetValue(100, 2); // numbers[2] = 100

```

### CopyTo

El método `CopyTo` copia todos los elementos del array actual a un array especificado empezando a partir de un índice determinado.

```csharp
int[] sourceArray = { 1, 2, 3 };
int[] destinationArray = new int[5];
sourceArray.CopyTo(destinationArray, 2);
// destinationArray = { 0, 0, 1, 2, 3 }

```

### Clone

El método `Clone` crea una copia superficial (*shallow copy*) del array.

```csharp
int[] numbers = { 10, 20, 30 };
int[] clonedArray = (int[]) numbers.Clone();

```

### Sort

El método `Sort` ordena los elementos de un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Sort(numbers); // numbers = { 10, 20, 30 }

```

### Reverse

El método `Reverse` invierte el orden de los elementos en un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Reverse(numbers); // numbers = { 20, 10, 30 }

```

### IndexOf

El método `IndexOf` devuelve el índice de la primera ocurrencia de un valor en un array unidimensional.

```csharp
int[] numbers = { 10, 20, 30 };
int index = Array.IndexOf(numbers, 20); // index = 1

```

### Find

El método `Find` devuelve el primer elemento que coincide con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30 };
int result = Array.Find(numbers, element => element > 15); // result = 20

```

### FindAll

El método `FindAll` devuelve todos los elementos que coinciden con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30, 40 };
int[] results = Array.FindAll(numbers, element => element > 15); // results = { 20, 30, 40 }

```

```

``````markdown
# Métodos y Propiedades de los Arrays en C#

## Propiedades

### Length
La propiedad `Length` obtiene el número total de elementos en todas las dimensiones del array.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int length = numbers.Length; // length = 5

```

### Rank

La propiedad `Rank` obtiene el número de dimensiones (o rango) del array.

```csharp
int[,] matrix = new int[3, 5];
int rank = matrix.Rank; // rank = 2

```

---

## Métodos

### GetValue y SetValue

El método `GetValue` obtiene el valor de una posición específica en el array y el método `SetValue` asigna un valor en una posición específica.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int value = (int) numbers.GetValue(2); // value = 30
numbers.SetValue(100, 2); // numbers[2] = 100

```

### CopyTo

El método `CopyTo` copia todos los elementos del array actual a un array especificado empezando a partir de un índice determinado.

```csharp
int[] sourceArray = { 1, 2, 3 };
int[] destinationArray = new int[5];
sourceArray.CopyTo(destinationArray, 2);
// destinationArray = { 0, 0, 1, 2, 3 }

```

### Clone

El método `Clone` crea una copia superficial (*shallow copy*) del array.

```csharp
int[] numbers = { 10, 20, 30 };
int[] clonedArray = (int[]) numbers.Clone();

```

### Sort

El método `Sort` ordena los elementos de un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Sort(numbers); // numbers = { 10, 20, 30 }

```

### Reverse

El método `Reverse` invierte el orden de los elementos en un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Reverse(numbers); // numbers = { 20, 10, 30 }

```

### IndexOf

El método `IndexOf` devuelve el índice de la primera ocurrencia de un valor en un array unidimensional.

```csharp
int[] numbers = { 10, 20, 30 };
int index = Array.IndexOf(numbers, 20); // index = 1

```

### Find

El método `Find` devuelve el primer elemento que coincide con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30 };
int result = Array.Find(numbers, element => element > 15); // result = 20

```

### FindAll

El método `FindAll` devuelve todos los elementos que coinciden con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30, 40 };
int[] results = Array.FindAll(numbers, element => element > 15); // results = { 20, 30, 40 }

```

```

``````markdown
# Métodos y Propiedades de los Arrays en C#

## Propiedades

### Length
La propiedad `Length` obtiene el número total de elementos en todas las dimensiones del array.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int length = numbers.Length; // length = 5

```

### Rank

La propiedad `Rank` obtiene el número de dimensiones (o rango) del array.

```csharp
int[,] matrix = new int[3, 5];
int rank = matrix.Rank; // rank = 2

```

---

## Métodos

### GetValue y SetValue

El método `GetValue` obtiene el valor de una posición específica en el array y el método `SetValue` asigna un valor en una posición específica.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int value = (int) numbers.GetValue(2); // value = 30
numbers.SetValue(100, 2); // numbers[2] = 100

```

### CopyTo

El método `CopyTo` copia todos los elementos del array actual a un array especificado empezando a partir de un índice determinado.

```csharp
int[] sourceArray = { 1, 2, 3 };
int[] destinationArray = new int[5];
sourceArray.CopyTo(destinationArray, 2);
// destinationArray = { 0, 0, 1, 2, 3 }

```

### Clone

El método `Clone` crea una copia superficial (*shallow copy*) del array.

```csharp
int[] numbers = { 10, 20, 30 };
int[] clonedArray = (int[]) numbers.Clone();

```

### Sort

El método `Sort` ordena los elementos de un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Sort(numbers); // numbers = { 10, 20, 30 }

```

### Reverse

El método `Reverse` invierte el orden de los elementos en un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Reverse(numbers); // numbers = { 20, 10, 30 }

```

### IndexOf

El método `IndexOf` devuelve el índice de la primera ocurrencia de un valor en un array unidimensional.

```csharp
int[] numbers = { 10, 20, 30 };
int index = Array.IndexOf(numbers, 20); // index = 1

```

### Find

El método `Find` devuelve el primer elemento que coincide con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30 };
int result = Array.Find(numbers, element => element > 15); // result = 20

```

### FindAll

El método `FindAll` devuelve todos los elementos que coinciden con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30, 40 };
int[] results = Array.FindAll(numbers, element => element > 15); // results = { 20, 30, 40 }

```

```

``````markdown
# Métodos y Propiedades de los Arrays en C#

## Propiedades

### Length
La propiedad `Length` obtiene el número total de elementos en todas las dimensiones del array.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int length = numbers.Length; // length = 5

```

### Rank

La propiedad `Rank` obtiene el número de dimensiones (o rango) del array.

```csharp
int[,] matrix = new int[3, 5];
int rank = matrix.Rank; // rank = 2

```

---

## Métodos

### GetValue y SetValue

El método `GetValue` obtiene el valor de una posición específica en el array y el método `SetValue` asigna un valor en una posición específica.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
int value = (int) numbers.GetValue(2); // value = 30
numbers.SetValue(100, 2); // numbers[2] = 100

```

### CopyTo

El método `CopyTo` copia todos los elementos del array actual a un array especificado empezando a partir de un índice determinado.

```csharp
int[] sourceArray = { 1, 2, 3 };
int[] destinationArray = new int[5];
sourceArray.CopyTo(destinationArray, 2);
// destinationArray = { 0, 0, 1, 2, 3 }

```

### Clone

El método `Clone` crea una copia superficial (*shallow copy*) del array.

```csharp
int[] numbers = { 10, 20, 30 };
int[] clonedArray = (int[]) numbers.Clone();

```

### Sort

El método `Sort` ordena los elementos de un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Sort(numbers); // numbers = { 10, 20, 30 }

```

### Reverse

El método `Reverse` invierte el orden de los elementos en un array unidimensional.

```csharp
int[] numbers = { 30, 10, 20 };
Array.Reverse(numbers); // numbers = { 20, 10, 30 }

```

### IndexOf

El método `IndexOf` devuelve el índice de la primera ocurrencia de un valor en un array unidimensional.

```csharp
int[] numbers = { 10, 20, 30 };
int index = Array.IndexOf(numbers, 20); // index = 1

```

### Find

El método `Find` devuelve el primer elemento que coincide con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30 };
int result = Array.Find(numbers, element => element > 15); // result = 20

```

### FindAll

El método `FindAll` devuelve todos los elementos que coinciden con las condiciones definidas por el predicado especificado.

```csharp
int[] numbers = { 10, 20, 30, 40 };
int[] results = Array.FindAll(numbers, element => element > 15); // results = { 20, 30, 40 }

```

```

```