En C#, cuando quieres convertir **un tipo numérico a otro tipo numérico**, normalmente tienes dos formas principales: **conversión implícita** y **conversión explícita (casting)**.

### 1. Conversión implícita

C# puede convertir automáticamente algunos tipos cuando la conversión es segura y no debería perder información.

```csharp
int numero = 10;

double resultado = numero;
```

Aquí:

```text
int → double
```

C# lo hace automáticamente.

Por ejemplo:

```csharp
int numero = 10;
double resultado = numero;

Console.WriteLine(resultado); // 10
```

---

### 2. Conversión explícita — casting

Cuando puede existir pérdida de información, debes indicarle explícitamente a C# que quieres realizar la conversión:

```csharp
double numero = 10.8;

int resultado = (int)numero;
```

Resultado:

```text
10
```

⚠️ **No redondea**, simplemente elimina la parte decimal.

```text
10.8
 ↓
(int)
 ↓
10
```

La sintaxis es:

```csharp
(tipoDestino)valor
```

Por ejemplo:

```csharp
double x = 10.5;

int a = (int)x;
decimal b = (decimal)x;
float c = (float)x;
```

---

### 🔥 Esto también explica tu ejercicio anterior

Si tienes:

```csharp
int numero1 = 5;
int numero2 = 2;
```

y haces:

```csharp
double resultado = numero1 / numero2;
```

❌ Obtienes:

```text
2
```

porque **la división ocurre primero como `int`**.

En cambio:

```csharp
double resultado = (double)numero1 / numero2;
```

✅ Obtienes:

```text
2.5
```

porque convertiste `numero1` a `double` **antes de realizar la división**.

### 🧠 Regla para recordar

> **Para convertir un número a otro tipo numérico puedes usar casting: `(tipoDestino)valor`. Si C# considera que la conversión es segura, puede hacerla implícitamente; si puede haber pérdida de información, normalmente necesitas hacerla explícita.**

Ejemplo rápido:

```text
int → double    ✅ implícita
double → int    ⚠️ explícita
int → float     ✅ implícita
float → int     ⚠️ explícita
```

## Sí, **puedes hacer la conversión directamente dentro de `Console.WriteLine()`**. No es obligatorio crear una variable nueva antes.

Lo importante es distinguir **cuándo ocurre la conversión respecto a la operación**.

### ✅ Puedes convertir dentro de `WriteLine`

Por ejemplo:

```csharp
int numero1 = 5;
int numero2 = 2;

Console.WriteLine((double)numero1 / numero2);
```

Aquí la conversión ocurre **dentro de la expresión**, antes de la división:

```text
(double)numero1
       ↓
     5.0
       ↓
  5.0 / 2
       ↓
    2.5
       ↓
Console.WriteLine()
```

---

### ❌ Pero esto es diferente

```csharp
Console.WriteLine((double)(numero1 / numero2));
```

Aquí primero ocurre:

```text
numero1 / numero2
     ↓
   5 / 2
     ↓
     2
```

Y **después** conviertes:

```text
2 → 2.0
```

Por lo tanto, imprime:

```text
2
```

No `2.5`.

### 🔥 Esta es la clave

No es que la conversión **tenga que hacerse antes de imprimir**.

Tiene que hacerse **antes de la operación en la que necesitas que participe ese tipo de dato**.

Puedes hacerlo:

```csharp
double resultado = (double)numero1 / numero2;
Console.WriteLine(resultado);
```

O directamente:

```csharp
Console.WriteLine((double)numero1 / numero2);
```

Ambas producen:

```text
2.5
```

### 🧠 Regla para tus apuntes

> **Una conversión de tipo puede realizarse directamente dentro de una expresión. Lo importante es que la conversión ocurra antes de la operación cuyo resultado queremos obtener con el nuevo tipo.**

Esto es muy importante porque posteriormente vas a encontrarte expresiones mucho más complejas, donde **la posición de una conversión puede cambiar completamente el resultado**.
