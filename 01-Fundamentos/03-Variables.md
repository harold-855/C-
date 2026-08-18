[Anterior ⬅️](./02-Sintaxis.md) | [Siguiente ➡️](./04-Constantes.md)
# Variable

Una variable, es un espacio de almacenamiento en la memoria que tiene un nombre y un tipo de datos asociados. Las variables permiten almacenar y manipular datos en tu aplicación. En C#, para declarar una variable, debes especificar su tipo seguido de un nombre. Puedes inicializar la variable, en el mismo momento de su declaración o hacerlo más adelante. (C# Guide, 2023)

## 📌 Variable declarada vs. variable inicializada

### 📝 Variable declarada

Una variable está **declarada** cuando indicamos su **tipo y nombre**, pero todavía no le asignamos un valor.

```csharp
int edad;
```

```
int → tipo de dato.
edad → nombre de la variable.
No tiene un valor asignado.
```

### 🚀 Variable inicializada

Una variable está inicializada cuando, además de declararla, le asignamos un valor inicial.

```
int edad = 27;
```
```
int → tipo de dato.
edad → nombre de la variable.
= → operador de asignación.
27 → valor inicial.
```

### 🔎 Diferencia

| Declarada | Inicializada |
|-----------|--------------|
| `int edad;` | `int edad = 27;` |
| Tiene tipo y nombre | Tiene tipo, nombre y valor |
| No tiene valor asignado | Tiene un valor inicial |

> 💡 **En resumen:** declarar es crear la variable; inicializar es darle su primer valor.

#### Uso de var para la declaracion de variables

C# es un lenguaje tipado, lo que significa que el tipo de una variable debe declararse de forma explícita o inferirse mediante la palabra clave var, la cual permite que el compilador determine automáticamente el tipo de la variable. (C# Guide, 2023) 

```
var message = "Hello, world;
```

💡 Piensa en var como: "C# descubre el tipo por mí", no como "esta variable puede cambiar de tipo".

var dato = "7";

dato = 7; // ❌ Error


Claro. Esto que acabas de aprender se llama **asignación de variables** y es importante diferenciarlo de la **declaración** e **inicialización**.

# 📌 Asignación de variables en C#

En C#, una variable se **declara** una sola vez dentro de su ámbito. Después de haber sido declarada, podemos cambiar su contenido mediante una **asignación**, sin necesidad de volver a escribir su tipo de dato.

## 🔹 Declaración e inicialización

```csharp
string nombre = "harold";
```

En esta línea:

* `string` → indica el **tipo de dato**.
* `nombre` → es el **nombre de la variable**.
* `"harold"` → es el **valor inicial**.

Aquí estamos **declarando e inicializando** la variable al mismo tiempo.

---

## 🔄 Asignación de un nuevo valor

Una vez creada la variable, podemos cambiar su valor:

```csharp
nombre = "HAROLD";
```

No escribimos nuevamente `string` porque `nombre` **ya existe y su tipo ya fue definido**.

También podemos asignarle el resultado de un método:

```csharp
nombre = nombre.ToUpper();
```

`ToUpper()` devuelve un nuevo `string` con los caracteres en mayúscula. El resultado se guarda nuevamente en `nombre`.

### Ejemplo completo

```csharp
string nombre = "harold";

nombre = nombre.ToUpper();

Console.WriteLine(nombre);
```

Resultado:

```text
HAROLD
```

---

## 🧠 Declaración vs. asignación

| Operación                    | Ejemplo                     | ¿Qué hace?                         |
| ---------------------------- | --------------------------- | ---------------------------------- |
| Declaración                  | `string nombre;`            | Crea la variable indicando su tipo |
| Inicialización               | `nombre = "harold";`        | Le asigna su primer valor          |
| Declaración + inicialización | `string nombre = "harold";` | Hace ambas operaciones             |
| Asignación                   | `nombre = "HAROLD";`        | Cambia el valor existente          |

### ⚠️ No confundas asignación con una nueva declaración

Correcto:

```csharp
string nombre = "harold";

nombre = nombre.ToUpper();
```

Incorrecto:

```csharp
string nombre = "harold";

string nombre = nombre.ToUpper();
```

En el segundo caso intentamos **declarar nuevamente una variable que ya existe** en el mismo ámbito.

> 💡 **Regla para recordar:** el tipo de dato se indica al declarar la variable. Cuando simplemente queremos cambiar su valor, utilizamos únicamente el nombre de la variable y el operador `=`.
