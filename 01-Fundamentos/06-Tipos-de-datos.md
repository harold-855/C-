[Anterior ⬅️](./05-Formatos-de-impresion.md) | [Siguiente ➡️](./07-Operaciones.md)



# tipos de datos


## Tipos numéricos enteros

| Tipo     | Tamaño  | Ejemplo                         | Rango aproximado                         |
|----------|---------|---------------------------------|-------------------------------------------|
| `sbyte`  | 8 bits  | `sbyte edad = 27;`              | -128 a 127                                |
| `byte`   | 8 bits  | `byte edad = 27;`               | 0 a 255                                   |
| `short`  | 16 bits | `short numero = 300;`           | -32 mil a 32 mil                          |
| `ushort` | 16 bits | `ushort numero = 300;`          | 0 a 65 mil                                |
| `int`    | 32 bits | `int edad = 27;`                | -2.1 mil millones a 2.1 mil millones      |
| `uint`   | 32 bits | `uint numero = 300;`            | 0 a 4.2 mil millones                      |
| `long`   | 64 bits | `long poblacion = 8000000000;`  | números muy grandes                       |
| `ulong`  | 64 bits | `ulong numero = 8000000000;`    | números positivos muy grandes             |


## Tipos numéricos con decimales

| Tipo      | Tamaño  | Precisión aproximada | Uso                              |
|-----------|---------|----------------------|----------------------------------|
| `float`   | 32 bits | ~6-9 dígitos         | Decimales                        |
| `double`  | 64 bits | ~15-17 dígitos       | Decimales, cálculos generales    |
| `decimal` | 128 bits | ~28-29 dígitos       | Dinero y cálculos financieros    |

## `float`

`float` se utiliza para almacenar **números con decimales** cuando no se necesita una precisión extremadamente alta.

### Condición para usar `float`

Se debe agregar el sufijo `f` o `F` al valor decimal para indicar explícitamente que es un `float`.

```csharp
float precio = 19.99f;
float altura = 1.75f;
```

## 🔤 3. `char`

Representa **un solo carácter**. 

```csharp
char letra = 'A';
char simbolo = '#';
char numero = '7';
```

### 🔤 Comillas en `char`

`char` utiliza **comillas simples** (`' '`), porque representa un solo carácter.

```csharp
char letra = 'A';
char simbolo = '#';
char numero = '7';
```

## 📝 4. `string`

Representa una **cadena de texto**, es decir, varios caracteres.

```csharp
string nombre = "Harold";
string ciudad = "Barranquilla";
string mensaje = "Hola mundo";
```

### 🔤 Comillas

Las cadenas de texto utilizan **comillas dobles**:

```csharp
"Hola"
```

Mientras que `char` utiliza **comillas simples**:

```csharp
'H'
```

> 💡 **Importante:** `string` puede contener varios caracteres, mientras que `char` representa únicamente un carácter.


## Tipo de dato booleano en C#

En C#, el tipo de dato booleano, representado por `bool`, se utiliza para almacenar **valores de verdad**: `true` (verdadero) o `false` (falso).

Este tipo de dato es fundamental en la programación, ya que se utiliza para **controlar el flujo de ejecución** mediante estructuras condicionales y bucles.

### Ejemplo

```csharp
bool isActive = true;
bool isComplete = false;
```

## 🔑 `Guid`


`Guid` Es un tipo de dato utilizado para representar un **identificador único**, normalmente usado para identificar registros, usuarios u objetos.


```csharp
Guid id = Guid.NewGuid();

Ejemplo de valor:

3f2504e0-4f89-41d3-9a0c-0305e82c3301
```

📦 object

object es el tipo base de todos los tipos de C#. Puede almacenar cualquier tipo de dato.

object dato = 25;
object nombre = "Harold";

💡 object puede almacenar diferentes tipos de valores, pero al recuperar el dato puede ser necesario hacer una conversión.