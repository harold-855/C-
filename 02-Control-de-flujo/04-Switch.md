[Anterior ⬅️](./03-Condicional-if-else.md) | [Siguiente ➡️](../03-Estructura-de-datos/01-Listas.md)

# ➡️ Switch

El switch evalúa una expresión y ejecuta el bloque de código correspondiente al caso que coincida con el valor de esa expresión. En lugar de ir probando múltiples condiciones con if y else if, el switch agrupa todo de manera más estructurada.

---

### 🔎 Sintaxis:

```csharp
switch (expression)
{
    case value1:
        // Código que se ejecuta si la expresión coincide con value1
        break;
    case value2:
        // Código que se ejecuta si la expresión coincide con value2
        break;
    default:
        // Código que se ejecuta si no coincide con ningún caso anterior
        break;
}
```
*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Sintaxis de la estructura switch*

---

### 💻 Ejemplo:

```csharp
int dayOfWeek = 3;

switch (dayOfWeek)
{
    case 1:
        Console.WriteLine("Monday");
        break;
    case 2:
        Console.WriteLine("Tuesday");
        break;
    case 3:
        Console.WriteLine("Wednesday");
        break;
    case 4:
        Console.WriteLine("Thursday");
        break;
    case 5:
        Console.WriteLine("Friday");
        break;
    default:
        Console.WriteLine("It's the weekend!");
        break;
}
```
*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo de la estructura switch*

**Explicación del flujo del ejemplo:**
En este ejemplo, la variable dayOfWeek tiene el valor 3, por lo que el bloque correspondiente a case 3 se ejecuta, imprimiendo "Wednesday". Si el valor de dayOfWeek hubiera sido otro número fuera del rango de 1 a 5, el bloque default se ejecutaría, mostrando "It's the weekend!".

---

### 📊 Características importantes del switch

* **case y break:** Cada caso dentro del switch se marca con la palabra clave case seguida del valor que deseas comparar. Después de ejecutar el código de un caso, se usa break para evitar que el programa continúe evaluando los demás casos.
* **default:** Es opcional, pero es una buena práctica incluirlo. Se ejecuta cuando ninguno de los casos coincide con el valor de la expresión, actuando como una especie de "else".
* **Tipos permitidos:** El switch en C# funciona con muchos tipos de datos, como int, char, string, y enum.
