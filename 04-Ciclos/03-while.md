# Ciclo while

El ciclo while, es una estructura de control que permite ejecutar un bloque de código mientras se cumpla una condición específica. A diferencia de los ciclos anteriores, donde puedes tener un número fijo de iteraciones, el ciclo while es ideal para situaciones en las que no sabes de antemano cuántas veces se ejecutará el bloque de código.

Sintaxis del ciclo while:

```csharp
while (condición)
{
    // Código a ejecutar mientras la condición sea verdadera
}

```

*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo de la sintaxis del ciclo while*

---

### Ejemplo de uso del ciclo while:

Imagina que deseas imprimir números del 1 al 5:

```csharp
int count = 1;

while (count <= 5)
{
    Console.WriteLine($"Count: {count}");
    count++;
}

```

*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo del ciclo while*

---

En este ejemplo, el ciclo while continuará ejecutándose mientras count sea menor o igual a 5, imprimiendo el valor de count en cada iteración.