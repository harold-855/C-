[Anterior ⬅️](./04-Constantes.md) | [Siguiente ➡️](./06-Tipos-de-datos.md)

# Formatos de impresión en C#

Para mostrar información en la consola, en C# utilizamos la clase `Console`, que ofrece varios métodos útiles para imprimir texto o valores en pantalla. *(Aplicativo de Consola - C#, 2023)*

## `Console.WriteLine(message)`

Imprime el valor que le pasas seguido de un salto de línea, moviendo el cursor a la siguiente línea.

### Ejemplo:

```csharp
Console.WriteLine("Hello world!");
```

`Console.Write(message)`

Imprime el valor, pero no agrega un salto de línea al final, permitiendo continuar en la misma línea.
```
Console.Write("Hello, ");
Console.WriteLine("world!");
```

### Interpolación de cadenas

Usando $ puedes insertar variables directamente en una cadena

```
string name = "John";
int age = 30;

Console.WriteLine($"Hello, my name is {name} and I am {age} years old");

```

💡 Nota: La interpolación de cadenas permite combinar texto y variables de una manera sencilla y legible utilizando $ antes de la cadena.



### 👀 Así quedaría la estructura

```
text
Formatos de impresión en C#
│
├── Console.WriteLine()
│   └── Imprime y salta de línea
│
├── Console.Write()
│   └── Imprime sin saltar de línea
│
└── Interpolación de cadenas
    └── Inserta variables usando $"{variable}"
```


