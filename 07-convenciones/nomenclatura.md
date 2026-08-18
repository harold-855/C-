# 1. Convenciones de nomenclatura en C#

Las convenciones de nomenclatura son reglas para **nombrar variables, métodos, clases, propiedades y otros elementos** del código. Su objetivo es que el código sea **claro, consistente y fácil de mantener**.

## 📌 Principales convenciones

| Elemento          | Convención         | Ejemplo               |
| ----------------- | ------------------ | --------------------- |
| Clases            | `PascalCase`       | `Usuario`, `Producto` |
| Métodos           | `PascalCase`       | `CalcularTotal()`     |
| Propiedades       | `PascalCase`       | `Nombre`, `Edad`      |
| Variables locales | `camelCase`        | `nombreUsuario`       |
| Parámetros        | `camelCase`        | `cantidadProductos`   |
| Constantes        | `PascalCase`       | `MaximoIntentos`      |
| Interfaces        | `PascalCase` + `I` | `IRepositorio`        |
| Campos privados   | `_camelCase`       | `_nombre`             |
| Enumeraciones     | `PascalCase`       | `EstadoUsuario`       |

## 🔹 PascalCase

Cada palabra comienza con mayúscula y no se utilizan espacios:

```csharp
public class Usuario
{
    public string NombreCompleto { get; set; }

    public void MostrarInformacion()
    {
    }
}
```

## 🔹 camelCase

La primera palabra comienza en minúscula y las siguientes en mayúscula:

```csharp
string nombreUsuario = "Harold";
int edadUsuario = 27;
```

## 🔹 Campos privados

Los campos privados normalmente utilizan `_` seguido de `camelCase`:

```csharp
private string _nombre;
private int _edad;
```

## 🔹 Constantes

Las constantes en C# normalmente siguen `PascalCase`:

```csharp
const int MaximoIntentos = 3;
const double Pi = 3.14159;
```

> 💡 **Regla rápida:**
>
> * **Clases, métodos y propiedades → `PascalCase`**
> * **Variables y parámetros → `camelCase`**
> * **Campos privados → `_camelCase`**
> * **Interfaces → `I` + `PascalCase`**
