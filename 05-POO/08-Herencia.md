# Herencia 

Herencia es un principio fundamental de la Programación Orientada a Objetos (POO) que permite que una clase nueva (llamada subclase o clase hija) herede las propiedades y métodos de una clase existente (llamada superclase o clase padre). 

Esto facilita la reutilización del código, ya que no tienes que reescribir funcionalidades comunes en cada nueva clase que crees. (Principios de La POO, 2022) 

En otras palabras, la herencia te permite crear una jerarquía de clases donde las clases derivadas pueden aprovechar lo que ya está definido en las clases superiores, añadiendo o modificando sus propios comportamientos si es necesario. 

Clase Base: Animal 


Subclase: Dog 

**Ventajas de la herencia**

* **Reutilización del código:** Las clases hijas pueden usar propiedades y métodos ya definidos en las clases padres.
* **Extensibilidad:** Las clases hijas pueden añadir nuevas funcionalidades sin afectar a las clases padres.
* **Organización:** Permite estructurar el código de forma más clara, dividiendo responsabilidades entre clases.

# Clase Base: Animal

La clase Animal es la clase base, que tiene propiedades comunes como Name y Age, y métodos como Eat y Sleep, en otras palabras, esta clase define propiedades y métodos comunes a todos los animales.

```csharp
public class Animal
{
    public string Name { get; set; }
    public int Age { get; set; }

    public void Eat()
    {
        Console.WriteLine($"{Name} is eating.");
    }

    public void Sleep()
    {
        Console.WriteLine($"{Name} is sleeping.");
    }
}

```

# Subclase: Dog

La clase Dog es la subclase, que hereda todas las propiedades y métodos de Animal y agrega un método específico para perros

```csharp
public class Dog : Animal
{
    public string Breed { get; set; }

    public void Bark()
    {
        Console.WriteLine($"{Name} is barking.");
    }
}

```

# Uso de la Herencia en Program.cs

Ahora vamos a crear una instancia de Dog en donde se le asignan valores a las propiedades heredadas y se llaman a los métodos heredados junto con el método específico de Dog.

```csharp
// Crear una instancia de la clase Dog (que hereda de Animal)
Dog myDog = new Dog();
myDog.Name = "Rex";
myDog.Age = 3;
myDog.Breed = "German Shepherd";

// Usar propiedades y métodos heredados de Animal
myDog.Eat();   // Rex is eating.
myDog.Sleep(); // Rex is sleeping.

// Usar el método específico de Dog
myDog.Bark();  // Rex is barking.

Console.WriteLine($"{myDog.Name} is a {myDog.Breed} and is {myDog.Age} years old.");

```

*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo de implementación de una clase Hija*

Este ejemplo muestra cómo una clase puede heredar características y comportamientos de otra, a la vez que añade su propia funcionalidad.

