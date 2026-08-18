# Tuplas en C#

Una **tupla** es una estructura ligera que agrupa varios valores de diferentes tipos en una sola unidad. A diferencia de las colecciones tradicionales (como arreglos o listas), permite combinar un conjunto fijo de datos sin necesidad de crear una clase dedicada.

---

## 1. Creación de una Tupla

Para crear una tupla, encierra los valores entre paréntesis separados por comas:

```csharp
var persona = ("Ana", 25);

Console.WriteLine(persona.Item1); // Output: Ana
Console.WriteLine(persona.Item2); // Output: 25

```

> **Nota:** Por defecto, los elementos se acceden mediante las propiedades genéricas `Item1`, `Item2`, `Item3`, etc.

---

## 2. Elementos Nombrados

Usar `ItemN` reduce la legibilidad del código. C# permite asignar nombres descriptivos a los campos:

```csharp
// Asignando nombres en el valor
var persona = (Nombre: "Ana", Edad: 25);

Console.WriteLine(persona.Nombre); // Output: Ana
Console.WriteLine(persona.Edad);   // Output: 25

```

También puedes definir los nombres directamente en el **tipo de la variable**:

```csharp
(string Nombre, int Edad) persona = ("Carlos", 30);

Console.WriteLine($"{persona.Nombre} tiene {persona.Edad} años.");

```

> 💡 **Buena Práctica**
> Prefiere siempre elementos nombrados sobre `Item1`, `Item2`. Una tupla como `(decimal Precio, int Cantidad)` se explica por sí sola, mientras que `(Item1, Item2)` obliga a adivinar su contenido.

---

## 3. Retornar Múltiples Valores desde un Método

Es el caso de uso más frecuente para las tuplas. Ofrece una alternativa limpia y moderna al uso de parámetros `out`:

```csharp
static (int Cociente, int Residuo) Dividir(int dividendo, int divisor)
{
    return (dividendo / divisor, dividendo % divisor);
}

// Invocación
var resultado = Dividir(17, 5);
Console.WriteLine($"Cociente: {resultado.Cociente}, Residuo: {resultado.Residuo}");
// Output: Cociente: 3, Residuo: 2

```

---

## 4. Desconstrucción (*Deconstruction*)

Puedes "desempaquetar" las partes de una tupla en variables individuales en una sola línea de código:

```csharp
var (nombre, edad) = ("Laura", 28);

Console.WriteLine(nombre); // Output: Laura
Console.WriteLine(edad);   // Output: 28

```

### Descarte de Valores (*Discards*)

Si solo necesitas parte de la información, ignora los valores no deseados mediante el símbolo de guion bajo `_`:

```csharp
var (cociente, _) = Dividir(17, 5); // El residuo es ignorado

```

---

## 5. Comparación de Tuplas

Dos tuplas son iguales (`==`) si todos sus elementos correspondientes son iguales en valor y orden:

```csharp
var puntoA = (2, 3);
var puntoB = (2, 3);

Console.WriteLine(puntoA == puntoB); // Output: True

```

---

## 6. Tuplas en Colecciones

Las tuplas se integran fácilmente con colecciones existentes para manejar listas de pares o grupos de datos temporales:

```csharp
var productos = new List<(string Nombre, decimal Precio)>
{
    ("Laptop", 1500.99m),
    ("Mouse", 25.50m),
    ("Teclado", 45.00m)
};

foreach (var (nombre, precio) in productos)
{
    Console.WriteLine($"{nombre}: {precio:C}");
}

```

---

> 📌 **¿Cuándo usar una Tupla vs. una Clase?**
> * **Tuplas:** Ideales para estructuras temporales, privadas o de alcance reducido dentro de un método.
> * **Clases / Records:** Recomendados si los datos tienen comportamiento propio (métodos, validaciones) o si se comparten públicamente a través de múltiples capas del sistema.
> 
>