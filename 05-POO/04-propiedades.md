# propiedades 

Las propiedades son las características que definen a un objeto. Siguiendo con el ejemplo del coche, podrías tener propiedades como el color, la marca y la velocidad máxima. En C#, puedes definir propiedades dentro de una clase utilizando métodos get y set, que permiten acceder y modificar estas propiedades de manera controlada. 

namespace ProjectName.Models;

```
public class Car
{
    // Propiedad para almacenar el color del coche
    public string Color { get; set; }

    // Propiedad para almacenar la marca del coche
    public string Brand { get; set; }

    // Propiedad para almacenar la velocidad máxima del coche
    public int MaxSpeed { get; set; }
}
```


Una vez que hayas definido las propiedades, puedes acceder a ellas mediante los métodos get y set. Aquí tienes un ejemplo de cómo crear una instancia de la clase Car y establecer sus propiedades desde la clase Program.cs, ten en cuenta que puedes acceder a clase desde cualquier lugar del programa, pero en este caso lo haremos desde Program.cs para facilitar el ejemplo: 

```
// 1. Importación del espacio de nombres donde reside la clase
using ProjectName.Models;

// 2. Creación de una nueva instancia del objeto 'Car'
Car myCar = new Car();

// 3. Asignación de valores a las propiedades del objeto
myCar.Color = "Rojo";
myCar.Brand = "Toyota";
myCar.MaxSpeed = 180;

// 4. Lectura de propiedades y salida en consola
Console.WriteLine($"My car is a {myCar.Brand} in color {myCar.Color} with a maximum speed of {myCar.MaxSpeed} km/h.");

```

Explicación del flujo:

using: Permite acceder a la clase Car ubicada en la carpeta/espacio de nombres ProjectName.Models.

new Car(): Reserva espacio en memoria y construye un objeto nuevo con la plantilla de la clase Car.

myCar.Propiedad: Utiliza el operador punto (.) tanto para asignar (set) como para leer (get) los atributos del vehículo.

En C#, **`get`** y **`set`** son bloques de código llamados **accesores** que se utilizan dentro de una **propiedad** para controlar cómo se leen (*get*) y cómo se escriben o modifican (*set*) los valores de las variables de una clase.

Serven para aplicar el principio de **encapsulamiento**, protegiendo la información y permitiendo validar datos antes de guardarlos.

---

### Conceptos Clave

* **`get` (Obtener):** Se ejecuta cuando **lees** o pides el valor de una propiedad. Devuelve el dato.
* **`set` (Establecer):** Se ejecuta cuando **asignas** o cambias el valor de una propiedad. Recibe el nuevo valor a través de la palabra clave implícita `value`.

---

### Comparación entre un campo público y una propiedad con Get/Set

**Sin Get/Set (Peligro de datos no válidos):**
Cualquiera puede asignar un valor absurdo desde fuera de la clase.

```csharp
public class Usuario
{
    public int Edad; // Campo público sin control
}

// Uso:
Usuario u = new Usuario();
u.Edad = -25; // ❌ Permite guardar números negativos sin control.

```

**Con Get/Set (Acceso controlado y seguro):**
Puedes interceptar la asignación y validar que los datos sean correctos.

```csharp
public class Usuario
{
    private int _edad; // Variable privada para almacenar el valor real

    public int Edad
    {
        get 
        { 
            return _edad; // Se activa al LEER: Console.WriteLine(u.Edad);
        }
        set 
        { 
            // Se activa al ESCRIBIR: u.Edad = 25;
            if (value < 0)
            {
                Console.WriteLine("La edad no puede ser negativa.");
            }
            else
            {
                _edad = value; // 'value' es el valor recibido
            }
        }
    }
}

```

---

### Resumen de Uso Corto (Propiedades Automáticas)

Si no necesitas agregar reglas o validaciones complejas, C# te permite escribir `get; set;` en una sola línea. El lenguaje creará la variable privada y la lógica básica de forma automática:

```csharp
public class Producto
{
    public string Nombre { get; set; } // Propiedad automática
    public double Precio { get; set; }
}

```