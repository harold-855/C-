# Encapsulamiento 

Una vez que hayas definido las propiedades, puedes acceder a ellas mediante los métodos get y set. Aquí tienes un ejemplo de cómo crear una instancia de la clase Car y establecer sus propiedades desde la clase Program.cs, ten en cuenta que puedes acceder a clase desde cualquier lugar del programa, pero en este caso lo haremos desde Program.cs para facilitar el ejemplo: 
Hacer clic sobre el boton para ver la informacion
El encapsulamiento es uno de los pilares fundamentales de la Programación Orientada a Objetos (POO). Este concepto se refiere a proteger el acceso a los datos internos de un objeto, permitiendo que solo se puedan acceder o modificar a través de métodos o propiedades controladas. De esta forma, los detalles internos de implementación quedan ocultos, y se asegura que los datos no sean alterados de manera inadecuada. (Rao & Nayak, 2014) 
clase Program.cs: 
En C#, esto se logra utilizando modificadores de acceso como private, protected y public, que controlan la visibilidad de las propiedades y métodos de una clase. 

**Beneficios del encapsulamiento**

* **Control:** Puedes controlar cómo se acceden y modifican las propiedades.
* **Seguridad:** Previene que los datos sean alterados de forma incorrecta.
* **Mantenimiento:** Permite cambiar la implementación interna sin afectar otras partes del código.

**Ejemplo de una clase con propiedades encapsuladas**

**Puntos informativos**

* **1. Propiedad pública:** accesible desde cualquier parte
* **2. Propiedad protegida:** accesible solo desde la clase o clases derivadas
* **3. Propiedad privada:** accesible solo dentro de esta clase
* **4. Podemos modificar Species desde dentro de la clase**



---

**Código C#**

```csharp
public class Animal
{


    public void SetSpecies(string species)
    {

    }

    public void ShowInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}, Species: {Species}");
    }
}

```

**clase Program.cs:**

**Puntos informativos**

* **1. Correcto:** Name es pública
* **2. Incorrecto:** Error, Age es protegida y no se puede acceder desde aquí
* **3. Incorrecto:** Error, Species es privada y no se puede acceder directamente
* **4. Correcto:** accedemos a la propiedad privada a través de un método público
* **5. Imprime:** "Name: Elephant, Age: 0, Species: Mammal"

*Hacer clic sobre el boton para ver la informacion*

---

**Código C#**

```csharp
Animal animal = new Animal();

// Acceso a la propiedad pública
animal.Name = "Elephant";

// Acceso a la propiedad protegida
animal.Age = 10;

// Acceso a la propiedad privada
animal.Species = "Mammal";

// Podemos usar métodos públicos que interactúan con propiedades protegidas o privadas
animal.SetSpecies("Mammal");

// Mostrar la información del animal
animal.ShowInfo();

```

---

Este ejemplo miramos cómo los distintos modificadores de acceso controlan quién puede acceder y modificar las propiedades de una clase. Esto es útil para proteger los datos sensibles y garantizar que se sigan reglas de negocio al modificar las propiedades de un objeto.