# ¿Qué es un Método?

Un método puede ser visto como una acción que un objeto puede realizar. Por ejemplo, si tienes una clase Car, podrías tener métodos como Accelerate() para aumentar la velocidad del coche o Brake() para reducirla.

Cómo Definir un Método

Para definir un método, se utiliza la siguiente sintaxis:

```csharp
public returnType MethodName (parameters)
{
    // Código del método
}

```

---

### Explicación paso a paso de la sintaxis:

1. **Definimos que el método será publico** entonces podemos usarlo cuando creemos una nueva instancia de la clase.
2. **Tipo de dato que devuelve el método** (puede ser void si no devuelve nada).
3. **Nombre que le das al método**, por lo general son acciones que puede hacer el objeto.
4. **Variables que le puedes pasar al método** (opcional).
5. **Definimos el contenido del método** dentro de llaves { }.

---

Continuando con nuestro ejemplo vamos a crear un método para mostrar la información del coche (**Car**):

```csharp
public void DisplayInfo()
{
    Console.WriteLine($"Este coche es un {Brand}, de color {Color}, y su velocidad máxima es {MaxSpeed} km/h.");
}

