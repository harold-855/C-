# abstraccion

La abstracción es un concepto fundamental en la Programación Orientada a Objetos que te permite ocultar los detalles complejos y mostrar solo lo necesario. Piensa en cómo utilizas un coche: conoces cómo conducirlo, pero no necesitas saber cómo funciona el motor o el sistema eléctrico en su interior. La abstracción permite simplificar la complejidad, enfocándose en lo esencial. (Molina, 2021) 

```csharp
public class Vehicle
{
    public string Brand { get; set; }
    public string Color { get; set; }
    public int MaxSpeed { get; set; }

    // Método para mostrar información del vehículo
    public void DisplayInfo()
    {
        Console.WriteLine($"Marca: {Brand}, Color: {Color}, Velocidad Máxima: {MaxSpeed} km/h");
    }
}

```

*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo de una clase con abstracción*

## clases abstractas 

Solo mantiene las propiedades más esenciales, esto simplifica el modelo y se enfoca en lo que realmente se necesita para las operaciones básicas que se van a realizar con el vehículo.


# Ejemplo de una Clase Abstracta

```csharp
namespace ProjectName.Models;

public abstract class Vehicle
{
    public string Brand { get; set; }
    public string Color { get; set; }

    // Método abstracto
    public abstract void Drive();

    // Método concreto
    public void DisplayInfo()
    {
        Console.WriteLine($"Este vehículo es un {Brand} de color {Color}.");
    }
}

```

*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo de una clase abstracta*

Esta clase contiene propiedades como Brand y Color, y un método abstracto Drive(), que no tiene implementación.

# Uso de la clase abstracta previamente creada

```csharp
public class Car : Vehicle
{
    public override void Drive()
    {
        Console.WriteLine("El coche está conduciendo.");
    }
}

```

*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo de uso de una clase abstracta*

Hereda de Vehicle y proporciona una implementación para el método Drive().

En resumen, la abstracción te permite diseñar tu código de manera más eficiente al separar la interfaz de la implementación. Al trabajar con clases abstractas, puedes definir comportamientos que deben ser implementados en las clases derivadas, lo que fomenta una estructura más clara y mantenible.
