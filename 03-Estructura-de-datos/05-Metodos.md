# Métodos en C#

**Organiza y reutiliza tu código**

En C#, los métodos son bloques de código que realizan una tarea específica. Son fundamentales para organizar tu código, mantenerlo limpio y evitar la repetición de instrucciones. Un método puede aceptar parámetros, realizar operaciones y devolver un valor, o 
implemente ejecutar una acción sin devolver nada.


---

### Sintaxis básica

```csharp
[ModificadorAcceso] [TipoRetorno] NombreDelMetodo([Parametros])
{
    // Bloque de código a ejecutar
    return [Valor]; // Solo si el TipoRetorno no es 'void'
}

tipoRetorno: Define el tipo de dato que el método devuelve. Si no devuelve nada, se usa 'void'.

NombreMetodo: Es el nombre del método, recuerda usar Pascal Case.

(parametros): Son las entradas que el método puede recibir, aunque puede estar vacío.

return valor;: Los métodos pueden retornar información pero esto es opcional ya que los métodos de tipo 'void' no retornan ningún valor.

```

---

### Ejemplo básico

```csharp
// Ejemplo de un método básico que suma dos números y devuelve un resultado
int Sumar(int a, int b)
{
    return a + b;
}

Los parámetros, permiten que los métodos acepten entradas y trabajen con valores específicos dentro de su ejecución. Estos parámetros se pasan como argumentos al momento de llamar al método. 

```

---

### Ejemplo de un método sin retorno (void)

```csharp
void Greet(string name)
{
    Console.WriteLine($"Hello, {name}!");
}

```
---

En C#, **`void`** es una palabra clave que se usa en la declaración de un método para indicar que **ese método no devuelve ningún valor**.

Cuando creas un método con `void`, le estás diciendo al programa: *"Ejecuta las instrucciones que están aquí dentro, pero al terminar, no me regreses ningún dato de vuelta"*.

---

### Comparación rápida: `void` vs Método con retorno

| Tipo de Método | ¿Devuelve valor? | Uso de `return` | Ejemplo de uso |
| --- | --- | --- | --- |
| **`void`** | ❌ No | Opcional (solo para salir antes) | Imprimir en pantalla, guardar un archivo, enviar un correo. |
| **`int` / `string` / etc.** | ✅ Sí | Obligatorio (`return valor;`) | Calcular una suma, consultar una base de datos. |

---

### Ejemplo práctico

```csharp
// Método VOID: Solo ejecuta una acción (imprime texto)
public void MostrarMensaje()
{
    Console.WriteLine("Proceso completado con éxito.");
    // No lleva 'return' de ningún valor
}

// Método CON RETORNO: Realiza un cálculo y te DEVUELVE un entero
public int ObtenerAnioActual()
{
    return 2026; // Es obligatorio devolver un número 'int'
}

```

### ¿Cómo los usas en el código?

```csharp
// 1. El método void solo se llama para ejecutar la acción:
MostrarMensaje(); 

// 2. El método con retorno te permite guardar lo que devuelve en una variable:
int anio = ObtenerAnioActual(); 

```


