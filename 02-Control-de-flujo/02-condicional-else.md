[Anterior ⬅️](./01-Condicional-if.md) | [Siguiente ➡️](./03-Condicional-if-else.md)

# ➡️ Condicional "else"

El **else** ejecuta un bloque de código alternativo cuando la condición del **if** resulta falsa.

---

### 🔎 Sintaxis General

```csharp
if (condition)
{
    // Código si la condición es VERDADERA
}
else
{
    // Código si la condición es FALSA
}
```
*Cómbita-Téllez, J. (2024). Sintaxis de la estructura If-else.*

---

### 💻 Ejemplo Práctico

```csharp
int age = 15;

if (age >= 18)
{
    Console.WriteLine("You are an adult.");
}
else
{
    Console.WriteLine("You are a minor.");
}
```
*Cómbita-Téllez, J. (2024). Ejemplo de la estructura If-else.*

---

### 📊 Explicación del Flujo

* **Evaluación**: El programa verifica si `age` (15) es mayor o igual a 18.
* **Resultado**: Como 15 no es mayor ni igual a 18, la condición es falsa.
* **Acción**: Salta el bloque `if` y ejecuta directamente el bloque `else`.
* **Salida en consola**: `"You are a minor."`
