[Anterior ⬅️](../01-Fundamentos/07-Operaciones.md) | [Siguiente ➡️](./02-condicional-else.md)

# Condicional `if` en C#

El `if` en C# es una **estructura condicional** que evalúa una expresión booleana. Si la expresión es verdadera (`true`), ejecuta el bloque de código dentro de las llaves `{}`.

Permite que el programa tome decisiones simples y responda de diferentes maneras según una condición.

## Sintaxis

```csharp
if (condicion)
{
    // Código que se ejecuta si la condición es verdadera
}
```

## Ejemplo

```csharp
int number = 10;

if (number > 5)
{
    Console.WriteLine("The number is greater than 5.");
}
```

En este ejemplo, como `number` tiene el valor `10` y `10 > 5` es verdadero, se ejecuta el código dentro del `if`.

> 💡 **En resumen:** `if` permite ejecutar un bloque de código **solo cuando una condición se cumple**.
