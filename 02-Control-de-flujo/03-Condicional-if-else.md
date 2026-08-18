# ➡️ Condicional else if

Pero ¿qué pasa cuando tienes más de una condición que revisar? Para eso tenemos el else if, que te permite manejar múltiples caminos posibles, una opción a la vez.

El else if te permite evaluar múltiples expresiones. Si la primera condición no se cumple, el programa intentará con las siguientes. Esto es útil cuando necesitas manejar varios casos específicos en una sola estructura.

---

### 🔎 Sintaxis:

```csharp
if (condition1)
{
    // Si condition1 es verdadera
}
else if (condition2)
{
    // Si condition1 es falsa, pero condition2 es verdadera
}
else
{
    // Si ninguna condición anterior es verdadera
}
```
*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Sintaxis de la estructura else-if*

**Explicación del flujo de sintaxis:**
Aquí, el programa está comprobando si age es mayor o igual a 18. Como age es 15, el mensaje que se imprime es: "You are a minor." Básicamente, estas cubriendo el caso donde la primera condición no se cumple.

---

### 💻 Ejemplo:

```csharp
int score = 85;

if (score >= 90)
{
    Console.WriteLine("You got an A!");
}
else if (score >= 80)
{
    Console.WriteLine("You got a B!");
}
else
{
    Console.WriteLine("You need to improve.");
}
```
*Cómbita-Téllez, J. (2024). Captura de pantalla del código, Ejemplo de la estructura else-if*

**Explicación del flujo del ejemplo:**
Aquí estamos evaluando tres posibilidades. Si la puntuación es mayor o igual a 90, imprime "You got an A!". Si no se cumple esa condición, osea el número NO es mayor o igual a 90 pero es mayor o igual a 80, imprime "You got a B!".

Ahora bien, si ninguna de esas condiciones se cumple, imprime "You need to improve." Es una forma genial de darle al código más de un camino, pero existe una alternativa para que no debas anidar muchos else-if, la cual verás a continuación:
