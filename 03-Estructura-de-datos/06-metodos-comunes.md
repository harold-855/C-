
# Métodos más usados en C#

Los métodos son bloques de código que realizan una tarea específica. En C# se utilizan constantemente para trabajar con texto, números, colecciones, conversiones y muchas otras operaciones.

---

## 🖥️ Métodos de `Console`

| Método | Descripción | Ejemplo |
|---|---|---|
| `Console.WriteLine()` | Muestra información y salta a la siguiente línea. | `Console.WriteLine("Hola");` |
| `Console.Write()` | Muestra información sin saltar de línea. | `Console.Write("Hola");` |
| `Console.ReadLine()` | Lee una línea introducida por el usuario. | `string nombre = Console.ReadLine();` |
| `Console.ReadKey()` | Espera a que el usuario presione una tecla. | `Console.ReadKey();` |

### Ejemplo

```csharp
Console.Write("¿Cuál es tu nombre? ");
string nombre = Console.ReadLine();

Console.WriteLine($"Hola, {nombre}");
````

---

# 🔄 Métodos de conversión

Se utilizan para convertir datos de un tipo a otro.

| Método               | Descripción                                                   | Ejemplo                              |
| -------------------- | ------------------------------------------------------------- | ------------------------------------ |
| `int.Parse()`        | Convierte un `string` a `int`.                                | `int.Parse("10")`                    |
| `double.Parse()`     | Convierte un `string` a `double`.                             | `double.Parse("10.5")`               |
| `decimal.Parse()`    | Convierte un `string` a `decimal`.                            | `decimal.Parse("10.5")`              |
| `bool.Parse()`       | Convierte un `string` a `bool`.                               | `bool.Parse("true")`                 |
| `Convert.ToInt32()`  | Convierte un valor a `int`.                                   | `Convert.ToInt32("10")`              |
| `Convert.ToDouble()` | Convierte un valor a `double`.                                | `Convert.ToDouble("10.5")`           |
| `Convert.ToString()` | Convierte un valor a `string`.                                | `Convert.ToString(10)`               |
| `ToString()`         | Convierte un valor en `string`.                               | `edad.ToString()`                    |
| `TryParse()`         | Intenta convertir un valor sin lanzar una excepción si falla. | `int.TryParse("10", out int numero)` |

### Ejemplo con `Parse()`

```csharp
string texto = "27";

int edad = int.Parse(texto);

Console.WriteLine(edad);
```

### Ejemplo con `TryParse()`

```csharp
string texto = "27";

if (int.TryParse(texto, out int edad))
{
    Console.WriteLine($"Edad: {edad}");
}
else
{
    Console.WriteLine("El valor no es válido.");
}
```

> 💡 **Recomendación:** `TryParse()` es más seguro cuando el valor proviene de una entrada del usuario.

---

# 🔤 Métodos de `string`

Los métodos de `string` permiten trabajar y modificar texto.

```csharp
string nombre = "Harold";
```

| Método         | Descripción                                      | Ejemplo                    |
| -------------- | ------------------------------------------------ | -------------------------- |
| `ToUpper()`    | Convierte a mayúsculas.                          | `nombre.ToUpper()`         |
| `ToLower()`    | Convierte a minúsculas.                          | `nombre.ToLower()`         |
| `Trim()`       | Elimina espacios al inicio y final.              | `nombre.Trim()`            |
| `Contains()`   | Comprueba si contiene un texto.                  | `nombre.Contains("Har")`   |
| `StartsWith()` | Comprueba si comienza con un texto.              | `nombre.StartsWith("H")`   |
| `EndsWith()`   | Comprueba si termina con un texto.               | `nombre.EndsWith("d")`     |
| `Replace()`    | Reemplaza un texto por otro.                     | `nombre.Replace("H", "J")` |
| `Substring()`  | Obtiene una parte del texto.                     | `nombre.Substring(0, 3)`   |
| `IndexOf()`    | Busca la posición de un texto.                   | `nombre.IndexOf("o")`      |
| `Contains()`   | Verifica si existe un elemento dentro del texto. | `nombre.Contains("a")`     |

### Ejemplo

```csharp
string nombre = " Harold ";

Console.WriteLine(nombre.Trim());
Console.WriteLine(nombre.ToUpper());
Console.WriteLine(nombre.ToLower());
Console.WriteLine(nombre.Contains("Harold"));
```

---

# 📋 Métodos de `List<T>`

Las listas permiten almacenar múltiples elementos.

```csharp
List<string> nombres = new List<string>();
```

| Método       | Descripción                          | Ejemplo                       |
| ------------ | ------------------------------------ | ----------------------------- |
| `Add()`      | Agrega un elemento.                  | `nombres.Add("Harold")`       |
| `Remove()`   | Elimina un elemento.                 | `nombres.Remove("Harold")`    |
| `RemoveAt()` | Elimina por índice.                  | `nombres.RemoveAt(0)`         |
| `Contains()` | Comprueba si existe un elemento.     | `nombres.Contains("Harold")`  |
| `Clear()`    | Elimina todos los elementos.         | `nombres.Clear()`             |
| `Insert()`   | Inserta un elemento en una posición. | `nombres.Insert(0, "Harold")` |
| `IndexOf()`  | Obtiene la posición de un elemento.  | `nombres.IndexOf("Harold")`   |

### Propiedades importantes

```csharp
nombres.Count;
```

> ⚠️ `Count` es una **propiedad**, no un método, porque no utiliza `()`.

### Ejemplo

```csharp
List<string> nombres = new List<string>();

nombres.Add("Harold");
nombres.Add("Carlos");
nombres.Add("Ana");

Console.WriteLine(nombres.Count);

nombres.Remove("Carlos");

Console.WriteLine(nombres.Contains("Ana"));
```

---

# 🔢 Métodos matemáticos `Math`

La clase `Math` proporciona métodos para realizar operaciones matemáticas.

| Método           | Descripción                | Ejemplo              |
| ---------------- | -------------------------- | -------------------- |
| `Math.Abs()`     | Obtiene el valor absoluto. | `Math.Abs(-10)`      |
| `Math.Max()`     | Obtiene el mayor valor.    | `Math.Max(10, 20)`   |
| `Math.Min()`     | Obtiene el menor valor.    | `Math.Min(10, 20)`   |
| `Math.Round()`   | Redondea un número.        | `Math.Round(10.6)`   |
| `Math.Floor()`   | Redondea hacia abajo.      | `Math.Floor(10.9)`   |
| `Math.Ceiling()` | Redondea hacia arriba.     | `Math.Ceiling(10.1)` |
| `Math.Pow()`     | Calcula una potencia.      | `Math.Pow(2, 3)`     |
| `Math.Sqrt()`    | Calcula una raíz cuadrada. | `Math.Sqrt(25)`      |

### Ejemplo

```csharp
double numero = -10.5;

Console.WriteLine(Math.Abs(numero));
Console.WriteLine(Math.Round(numero));
Console.WriteLine(Math.Sqrt(25));
Console.WriteLine(Math.Pow(2, 3));
```

---

# 🔍 Métodos de búsqueda y consulta

Son muy utilizados para trabajar con colecciones y datos.

```csharp
List<int> numeros = new List<int> { 10, 20, 30, 40 };
```

| Método       | Descripción                                                  |
| ------------ | ------------------------------------------------------------ |
| `Contains()` | Comprueba si existe un elemento.                             |
| `IndexOf()`  | Obtiene la posición de un elemento.                          |
| `Find()`     | Busca un elemento que cumpla una condición.                  |
| `FindAll()`  | Busca todos los elementos que cumplan una condición.         |
| `Any()`      | Comprueba si existe algún elemento que cumpla una condición. |
| `All()`      | Comprueba si todos cumplen una condición.                    |

### Ejemplo

```csharp
List<int> numeros = new List<int> { 10, 20, 30, 40 };

bool existe = numeros.Contains(20);

Console.WriteLine(existe);
```

---

# 📊 Métodos LINQ más usados

LINQ permite consultar y transformar colecciones.

```csharp
using System.Linq;
```

| Método                | Descripción                                   | Ejemplo                             |
| --------------------- | --------------------------------------------- | ----------------------------------- |
| `Where()`             | Filtra elementos.                             | `numeros.Where(n => n > 20)`        |
| `Select()`            | Transforma elementos.                         | `numeros.Select(n => n * 2)`        |
| `First()`             | Obtiene el primer elemento.                   | `numeros.First()`                   |
| `FirstOrDefault()`    | Obtiene el primero o el valor predeterminado. | `numeros.FirstOrDefault()`          |
| `Last()`              | Obtiene el último elemento.                   | `numeros.Last()`                    |
| `Count()`             | Cuenta elementos.                             | `numeros.Count()`                   |
| `Sum()`               | Calcula la suma.                              | `numeros.Sum()`                     |
| `Average()`           | Calcula el promedio.                          | `numeros.Average()`                 |
| `Max()`               | Obtiene el mayor.                             | `numeros.Max()`                     |
| `Min()`               | Obtiene el menor.                             | `numeros.Min()`                     |
| `OrderBy()`           | Ordena ascendentemente.                       | `numeros.OrderBy(n => n)`           |
| `OrderByDescending()` | Ordena descendentemente.                      | `numeros.OrderByDescending(n => n)` |

### Ejemplo

```csharp
List<int> numeros = new List<int>
{
    10, 20, 30, 40, 50
};

var mayores = numeros.Where(n => n > 25);

foreach (var numero in mayores)
{
    Console.WriteLine(numero);
}
```

---

# 🧩 Métodos de arrays

Los arrays tienen algunas operaciones comunes mediante `Array`.

```csharp
int[] numeros = { 10, 20, 30, 40 };
```

| Método            | Descripción                         |
| ----------------- | ----------------------------------- |
| `Array.Sort()`    | Ordena un array.                    |
| `Array.Reverse()` | Invierte el orden.                  |
| `Array.IndexOf()` | Busca la posición de un elemento.   |
| `Array.Clear()`   | Limpia los elementos.               |
| `Array.Copy()`    | Copia elementos de un array a otro. |

### Ejemplo

```csharp
int[] numeros = { 30, 10, 20 };

Array.Sort(numeros);

foreach (int numero in numeros)
{
    Console.WriteLine(numero);
}
```

Resultado:

```text
10
20
30
```

---

# 📅 Métodos de `DateTime`

Se utilizan para trabajar con fechas y horas.

```csharp
DateTime fecha = DateTime.Now;
```

| Método         | Descripción                 |
| -------------- | --------------------------- |
| `AddDays()`    | Agrega días.                |
| `AddMonths()`  | Agrega meses.               |
| `AddYears()`   | Agrega años.                |
| `AddHours()`   | Agrega horas.               |
| `AddMinutes()` | Agrega minutos.             |
| `ToString()`   | Convierte la fecha a texto. |

### Ejemplo

```csharp
DateTime fecha = DateTime.Now;

Console.WriteLine(fecha);
Console.WriteLine(fecha.AddDays(7));
Console.WriteLine(fecha.AddMonths(1));
```

---

# 🛠️ Métodos propios

En C# también puedes crear tus propios métodos.

```csharp
static void Saludar()
{
    Console.WriteLine("Hola Harold");
}
```

Para ejecutarlo:

```csharp
Saludar();
```

### Método con parámetros

```csharp
static void Saludar(string nombre)
{
    Console.WriteLine($"Hola {nombre}");
}
```

Uso:

```csharp
Saludar("Harold");
```

### Método con retorno

```csharp
static int Sumar(int numero1, int numero2)
{
    return numero1 + numero2;
}
```

Uso:

```csharp
int resultado = Sumar(10, 20);

Console.WriteLine(resultado);
```

Resultado:

```text
30
```

---

# ⭐ Métodos que debes aprender primero

Si estás comenzando con C#, prioriza estos:

### Consola

```text
Console.WriteLine()
Console.Write()
Console.ReadLine()
```

### Conversión

```text
int.Parse()
double.Parse()
Convert.ToInt32()
ToString()
TryParse()
```

### String

```text
ToUpper()
ToLower()
Trim()
Contains()
StartsWith()
EndsWith()
Replace()
Substring()
IndexOf()
```

### Listas

```text
Add()
Remove()
RemoveAt()
Contains()
Clear()
Insert()
IndexOf()
```

### Matemáticas

```text
Math.Abs()
Math.Max()
Math.Min()
Math.Round()
Math.Floor()
Math.Ceiling()
Math.Pow()
Math.Sqrt()
```

### LINQ

```text
Where()
Select()
First()
FirstOrDefault()
Last()
Count()
Sum()
Average()
Max()
Min()
OrderBy()
OrderByDescending()
```

---

## 💡 Método vs propiedad

Una diferencia importante:

```csharp
nombre.ToUpper();  // Método
nombre.Length;     // Propiedad

lista.Add("C#");   // Método
lista.Count;       // Propiedad
```

### Regla rápida

> **Método:** realiza una acción → `()`

> **Propiedad:** proporciona información sobre un objeto → normalmente no lleva `()`

---

## 🎯 Resumen

Los métodos más importantes para comenzar con C# son:

```text
Console.WriteLine()
Console.ReadLine()
Parse()
TryParse()
ToString()

ToUpper()
ToLower()
Trim()
Contains()
Replace()
Substring()

Add()
Remove()
RemoveAt()
Clear()
Contains()

Math.Max()
Math.Min()
Math.Round()
Math.Pow()
Math.Sqrt()

Where()
Select()
First()
FirstOrDefault()
Count()
Sum()
Average()
OrderBy()
```

> 🚀 **No necesitas memorizar todos los métodos.** Lo importante es entender qué hace cada uno y aprender a buscarlos cuando los necesites.

```
```
````markdown
# Métodos más usados en C#

Los métodos son bloques de código que realizan una tarea específica. En C# se utilizan constantemente para trabajar con texto, números, colecciones, conversiones y muchas otras operaciones.

---

## 🖥️ Métodos de `Console`

| Método | Descripción | Ejemplo |
|---|---|---|
| `Console.WriteLine()` | Muestra información y salta a la siguiente línea. | `Console.WriteLine("Hola");` |
| `Console.Write()` | Muestra información sin saltar de línea. | `Console.Write("Hola");` |
| `Console.ReadLine()` | Lee una línea introducida por el usuario. | `string nombre = Console.ReadLine();` |
| `Console.ReadKey()` | Espera a que el usuario presione una tecla. | `Console.ReadKey();` |

### Ejemplo

```csharp
Console.Write("¿Cuál es tu nombre? ");
string nombre = Console.ReadLine();

Console.WriteLine($"Hola, {nombre}");
````

---

# 🔄 Métodos de conversión

Se utilizan para convertir datos de un tipo a otro.

| Método               | Descripción                                                   | Ejemplo                              |
| -------------------- | ------------------------------------------------------------- | ------------------------------------ |
| `int.Parse()`        | Convierte un `string` a `int`.                                | `int.Parse("10")`                    |
| `double.Parse()`     | Convierte un `string` a `double`.                             | `double.Parse("10.5")`               |
| `decimal.Parse()`    | Convierte un `string` a `decimal`.                            | `decimal.Parse("10.5")`              |
| `bool.Parse()`       | Convierte un `string` a `bool`.                               | `bool.Parse("true")`                 |
| `Convert.ToInt32()`  | Convierte un valor a `int`.                                   | `Convert.ToInt32("10")`              |
| `Convert.ToDouble()` | Convierte un valor a `double`.                                | `Convert.ToDouble("10.5")`           |
| `Convert.ToString()` | Convierte un valor a `string`.                                | `Convert.ToString(10)`               |
| `ToString()`         | Convierte un valor en `string`.                               | `edad.ToString()`                    |
| `TryParse()`         | Intenta convertir un valor sin lanzar una excepción si falla. | `int.TryParse("10", out int numero)` |

### Ejemplo con `Parse()`

```csharp
string texto = "27";

int edad = int.Parse(texto);

Console.WriteLine(edad);
```

### Ejemplo con `TryParse()`

```csharp
string texto = "27";

if (int.TryParse(texto, out int edad))
{
    Console.WriteLine($"Edad: {edad}");
}
else
{
    Console.WriteLine("El valor no es válido.");
}
```

> 💡 **Recomendación:** `TryParse()` es más seguro cuando el valor proviene de una entrada del usuario.

---

# 🔤 Métodos de `string`

Los métodos de `string` permiten trabajar y modificar texto.

```csharp
string nombre = "Harold";
```

| Método         | Descripción                                      | Ejemplo                    |
| -------------- | ------------------------------------------------ | -------------------------- |
| `ToUpper()`    | Convierte a mayúsculas.                          | `nombre.ToUpper()`         |
| `ToLower()`    | Convierte a minúsculas.                          | `nombre.ToLower()`         |
| `Trim()`       | Elimina espacios al inicio y final.              | `nombre.Trim()`            |
| `Contains()`   | Comprueba si contiene un texto.                  | `nombre.Contains("Har")`   |
| `StartsWith()` | Comprueba si comienza con un texto.              | `nombre.StartsWith("H")`   |
| `EndsWith()`   | Comprueba si termina con un texto.               | `nombre.EndsWith("d")`     |
| `Replace()`    | Reemplaza un texto por otro.                     | `nombre.Replace("H", "J")` |
| `Substring()`  | Obtiene una parte del texto.                     | `nombre.Substring(0, 3)`   |
| `IndexOf()`    | Busca la posición de un texto.                   | `nombre.IndexOf("o")`      |
| `Contains()`   | Verifica si existe un elemento dentro del texto. | `nombre.Contains("a")`     |

### Ejemplo

```csharp
string nombre = " Harold ";

Console.WriteLine(nombre.Trim());
Console.WriteLine(nombre.ToUpper());
Console.WriteLine(nombre.ToLower());
Console.WriteLine(nombre.Contains("Harold"));
```

---

# 📋 Métodos de `List<T>`

Las listas permiten almacenar múltiples elementos.

```csharp
List<string> nombres = new List<string>();
```

| Método       | Descripción                          | Ejemplo                       |
| ------------ | ------------------------------------ | ----------------------------- |
| `Add()`      | Agrega un elemento.                  | `nombres.Add("Harold")`       |
| `Remove()`   | Elimina un elemento.                 | `nombres.Remove("Harold")`    |
| `RemoveAt()` | Elimina por índice.                  | `nombres.RemoveAt(0)`         |
| `Contains()` | Comprueba si existe un elemento.     | `nombres.Contains("Harold")`  |
| `Clear()`    | Elimina todos los elementos.         | `nombres.Clear()`             |
| `Insert()`   | Inserta un elemento en una posición. | `nombres.Insert(0, "Harold")` |
| `IndexOf()`  | Obtiene la posición de un elemento.  | `nombres.IndexOf("Harold")`   |

### Propiedades importantes

```csharp
nombres.Count;
```

> ⚠️ `Count` es una **propiedad**, no un método, porque no utiliza `()`.

### Ejemplo

```csharp
List<string> nombres = new List<string>();

nombres.Add("Harold");
nombres.Add("Carlos");
nombres.Add("Ana");

Console.WriteLine(nombres.Count);

nombres.Remove("Carlos");

Console.WriteLine(nombres.Contains("Ana"));
```

---

# 🔢 Métodos matemáticos `Math`

La clase `Math` proporciona métodos para realizar operaciones matemáticas.

| Método           | Descripción                | Ejemplo              |
| ---------------- | -------------------------- | -------------------- |
| `Math.Abs()`     | Obtiene el valor absoluto. | `Math.Abs(-10)`      |
| `Math.Max()`     | Obtiene el mayor valor.    | `Math.Max(10, 20)`   |
| `Math.Min()`     | Obtiene el menor valor.    | `Math.Min(10, 20)`   |
| `Math.Round()`   | Redondea un número.        | `Math.Round(10.6)`   |
| `Math.Floor()`   | Redondea hacia abajo.      | `Math.Floor(10.9)`   |
| `Math.Ceiling()` | Redondea hacia arriba.     | `Math.Ceiling(10.1)` |
| `Math.Pow()`     | Calcula una potencia.      | `Math.Pow(2, 3)`     |
| `Math.Sqrt()`    | Calcula una raíz cuadrada. | `Math.Sqrt(25)`      |

### Ejemplo

```csharp
double numero = -10.5;

Console.WriteLine(Math.Abs(numero));
Console.WriteLine(Math.Round(numero));
Console.WriteLine(Math.Sqrt(25));
Console.WriteLine(Math.Pow(2, 3));
```

---

# 🔍 Métodos de búsqueda y consulta

Son muy utilizados para trabajar con colecciones y datos.

```csharp
List<int> numeros = new List<int> { 10, 20, 30, 40 };
```

| Método       | Descripción                                                  |
| ------------ | ------------------------------------------------------------ |
| `Contains()` | Comprueba si existe un elemento.                             |
| `IndexOf()`  | Obtiene la posición de un elemento.                          |
| `Find()`     | Busca un elemento que cumpla una condición.                  |
| `FindAll()`  | Busca todos los elementos que cumplan una condición.         |
| `Any()`      | Comprueba si existe algún elemento que cumpla una condición. |
| `All()`      | Comprueba si todos cumplen una condición.                    |

### Ejemplo

```csharp
List<int> numeros = new List<int> { 10, 20, 30, 40 };

bool existe = numeros.Contains(20);

Console.WriteLine(existe);
```

---

# 📊 Métodos LINQ más usados

LINQ permite consultar y transformar colecciones.

```csharp
using System.Linq;
```

| Método                | Descripción                                   | Ejemplo                             |
| --------------------- | --------------------------------------------- | ----------------------------------- |
| `Where()`             | Filtra elementos.                             | `numeros.Where(n => n > 20)`        |
| `Select()`            | Transforma elementos.                         | `numeros.Select(n => n * 2)`        |
| `First()`             | Obtiene el primer elemento.                   | `numeros.First()`                   |
| `FirstOrDefault()`    | Obtiene el primero o el valor predeterminado. | `numeros.FirstOrDefault()`          |
| `Last()`              | Obtiene el último elemento.                   | `numeros.Last()`                    |
| `Count()`             | Cuenta elementos.                             | `numeros.Count()`                   |
| `Sum()`               | Calcula la suma.                              | `numeros.Sum()`                     |
| `Average()`           | Calcula el promedio.                          | `numeros.Average()`                 |
| `Max()`               | Obtiene el mayor.                             | `numeros.Max()`                     |
| `Min()`               | Obtiene el menor.                             | `numeros.Min()`                     |
| `OrderBy()`           | Ordena ascendentemente.                       | `numeros.OrderBy(n => n)`           |
| `OrderByDescending()` | Ordena descendentemente.                      | `numeros.OrderByDescending(n => n)` |

### Ejemplo

```csharp
List<int> numeros = new List<int>
{
    10, 20, 30, 40, 50
};

var mayores = numeros.Where(n => n > 25);

foreach (var numero in mayores)
{
    Console.WriteLine(numero);
}
```

---

# 🧩 Métodos de arrays

Los arrays tienen algunas operaciones comunes mediante `Array`.

```csharp
int[] numeros = { 10, 20, 30, 40 };
```

| Método            | Descripción                         |
| ----------------- | ----------------------------------- |
| `Array.Sort()`    | Ordena un array.                    |
| `Array.Reverse()` | Invierte el orden.                  |
| `Array.IndexOf()` | Busca la posición de un elemento.   |
| `Array.Clear()`   | Limpia los elementos.               |
| `Array.Copy()`    | Copia elementos de un array a otro. |

### Ejemplo

```csharp
int[] numeros = { 30, 10, 20 };

Array.Sort(numeros);

foreach (int numero in numeros)
{
    Console.WriteLine(numero);
}
```

Resultado:

```text
10
20
30
```

---

# 📅 Métodos de `DateTime`

Se utilizan para trabajar con fechas y horas.

```csharp
DateTime fecha = DateTime.Now;
```

| Método         | Descripción                 |
| -------------- | --------------------------- |
| `AddDays()`    | Agrega días.                |
| `AddMonths()`  | Agrega meses.               |
| `AddYears()`   | Agrega años.                |
| `AddHours()`   | Agrega horas.               |
| `AddMinutes()` | Agrega minutos.             |
| `ToString()`   | Convierte la fecha a texto. |

### Ejemplo

```csharp
DateTime fecha = DateTime.Now;

Console.WriteLine(fecha);
Console.WriteLine(fecha.AddDays(7));
Console.WriteLine(fecha.AddMonths(1));
```

---

# 🛠️ Métodos propios

En C# también puedes crear tus propios métodos.

```csharp
static void Saludar()
{
    Console.WriteLine("Hola Harold");
}
```

Para ejecutarlo:

```csharp
Saludar();
```

### Método con parámetros

```csharp
static void Saludar(string nombre)
{
    Console.WriteLine($"Hola {nombre}");
}
```

Uso:

```csharp
Saludar("Harold");
```

### Método con retorno

```csharp
static int Sumar(int numero1, int numero2)
{
    return numero1 + numero2;
}
```

Uso:

```csharp
int resultado = Sumar(10, 20);

Console.WriteLine(resultado);
```

Resultado:

```text
30
```

---

# ⭐ Métodos que debes aprender primero

Si estás comenzando con C#, prioriza estos:

### Consola

```text
Console.WriteLine()
Console.Write()
Console.ReadLine()
```

### Conversión

```text
int.Parse()
double.Parse()
Convert.ToInt32()
ToString()
TryParse()
```

### String

```text
ToUpper()
ToLower()
Trim()
Contains()
StartsWith()
EndsWith()
Replace()
Substring()
IndexOf()
```

### Listas

```text
Add()
Remove()
RemoveAt()
Contains()
Clear()
Insert()
IndexOf()
```

### Matemáticas

```text
Math.Abs()
Math.Max()
Math.Min()
Math.Round()
Math.Floor()
Math.Ceiling()
Math.Pow()
Math.Sqrt()
```

### LINQ

```text
Where()
Select()
First()
FirstOrDefault()
Last()
Count()
Sum()
Average()
Max()
Min()
OrderBy()
OrderByDescending()
```

---

## 💡 Método vs propiedad

Una diferencia importante:

```csharp
nombre.ToUpper();  // Método
nombre.Length;     // Propiedad

lista.Add("C#");   // Método
lista.Count;       // Propiedad
```

### Regla rápida

> **Método:** realiza una acción → `()`

> **Propiedad:** proporciona información sobre un objeto → normalmente no lleva `()`

---

## 🎯 Resumen

Los métodos más importantes para comenzar con C# son:

```text
Console.WriteLine()
Console.ReadLine()
Parse()
TryParse()
ToString()

ToUpper()
ToLower()
Trim()
Contains()
Replace()
Substring()

Add()
Remove()
RemoveAt()
Clear()
Contains()

Math.Max()
Math.Min()
Math.Round()
Math.Pow()
Math.Sqrt()

Where()
Select()
First()
FirstOrDefault()
Count()
Sum()
Average()
OrderBy()
```

> 🚀 **No necesitas memorizar todos los métodos.** Lo importante es entender qué hace cada uno y aprender a buscarlos cuando los necesites.

```
```
