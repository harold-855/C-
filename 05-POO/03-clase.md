# Estructura de la clase es la siguiente

```csharp
namespace ProjectName.Models
{
    public class Car
    {
        // content of the class
    }
}

```

---

### Explicación paso a paso de cada parte

* **`namespace` (Espacio de nombres):** En C#, un namespace es una forma de organizar y agrupar clases, interfaces, estructuras, enumeraciones y otros tipos de datos relacionados. Se utiliza para evitar conflictos de nombres y mejorar la legibilidad del código.
* **`ProjectName.Models`:** En este caso se indica que la clase `Car` pertenece a un proyecto específico (`ProjectName`) y a un grupo específico de clases relacionadas con modelos (`Models`), en otras palabras que la clase `Car` está dentro de la carpeta `Models`.
* **`public` (Modificador de acceso):** Luego indicamos que la clase es pública, o sea que ella puede ser llamada desde cualquier lugar del programa.
* **`class` (Palabra clave):** Ahora indicamos que vamos a crear una clase usando la palabra clave `class`.
* **`Car` (Nombre de la clase):** Luego nombramos la clase. Las buenas prácticas recomiendan nombrar a las clases usando *PascalCase* y en singular, ya que las clases son el molde para crear nuevos objetos, entonces a partir de un molde se crean muchos objetos.
* **`{ }` (Llaves del cuerpo):** Después abrimos y cerramos llaves `{ }`. Dentro de esas llaves vamos a poner todo el contenido de nuestra clase (`// content of the class`).