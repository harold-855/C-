UML (**Unified Modeling Language**) es el lenguaje estándar para visualizar, especificar, construir y documentar la estructura y diseño de un sistema de software.

Dentro de UML, el **diagrama de clases** es el más utilizado. Muestra la estructura estática del sistema representando sus clases, atributos, métodos y cómo se relacionan entre sí.

---

**1. Estructura de una Clase en UML**

Una clase se dibuja como un rectángulo dividido en tres secciones:

```text
+-----------------------------------+
|            NombreClase            |
+-----------------------------------+
| - atributoPrivado: Tipo           |
| + atributoPublico: Tipo           |
| # atributoProtegido: Tipo         |
+-----------------------------------+
| + metodoPublico(param: Tipo): Tipo|
| - metodoPrivado(): void           |
+-----------------------------------+

```

**Símbolos de Visibilidad:**

* `+` **Público:** Accesible desde cualquier clase.
* `-` **Privado:** Accesible solo dentro de la misma clase.
* `#` **Protegido:** Accesible por la clase y sus subclases.
* `~` **Paquete / Interno:** Accesible por clases dentro del mismo espacio de nombres.

---

**2. Principales Relaciones entre Clases**

| Relación | Conector en Diagrama | Significado |
| --- | --- | --- |
| **Herencia** | Línea con flecha blanca `───▷` | Una clase deriva de otra (ej. *Perro* hereda de *Animal*). |
| **Asociación** | Línea continua `──────` | Relación básica entre dos clases independientes (ej. *Cliente* realiza *Pedido*). |
| **Agregación** | Línea con diamante vacío `───◇` | Relación "tiene un", donde la parte puede existir sin el todo (ej. *Universidad* tiene *Profesores*). |
| **Composición** | Línea con diamante lleno `───◆` | Relación fuerte donde la parte NO existe sin el todo (ej. *Casa* tiene *Habitaciones*). |
| **Dependencia** | Línea punteada con flecha `┈┈┈❯` | Una clase usa temporalmente a otra (ej. una clase usa una interfaz o parámetro). |

---

**3. Pasos para Crear un Diagrama de Clases**

1. **Identificar los sustantivos (Clases):** Lee los requerimientos del sistema y extrae los conceptos principales (ej. *Usuario*, *Factura*, *Producto*).
2. **Definir los atributos:** Determina qué datos necesita almacenar cada clase (ej. *Factura* necesita *fecha*, *total*).
3. **Definir los métodos:** Determina las acciones que realiza cada clase (ej. *Factura* tiene *calcularTotal()*).
4. **Establecer las relaciones y multiplicidad:** Conecta las clases indicando cuántas instancias participan en la relación (ej. `1` a `1..*` indica que un *Cliente* puede tener de 1 a muchos *Pedidos*).

---

**Ejemplo Práctico en Código C# vs UML**

Si traducimos el diagrama a código en C#:

```csharp
public class Cliente
{
    private string nombre;
    public List<Pedido> Pedidos { get; set; } = new();

    public void RealizarPedido(Pedido pedido)
    {
        Pedidos.Add(pedido);
    }
}

public class Pedido
{
    public int Id { get; set; }
    public decimal Total { get; set; }
}

```UML (**Unified Modeling Language**) es el lenguaje estándar para visualizar, especificar, construir y documentar la estructura y diseño de un sistema de software.

Dentro de UML, el **diagrama de clases** es el más utilizado. Muestra la estructura estática del sistema representando sus clases, atributos, métodos y cómo se relacionan entre sí.

---

**1. Estructura de una Clase en UML**

Una clase se dibuja como un rectángulo dividido en tres secciones:

```text
+-----------------------------------+
|            NombreClase            |
+-----------------------------------+
| - atributoPrivado: Tipo           |
| + atributoPublico: Tipo           |
| # atributoProtegido: Tipo         |
+-----------------------------------+
| + metodoPublico(param: Tipo): Tipo|
| - metodoPrivado(): void           |
+-----------------------------------+

```

**Símbolos de Visibilidad:**

* `+` **Público:** Accesible desde cualquier clase.
* `-` **Privado:** Accesible solo dentro de la misma clase.
* `#` **Protegido:** Accesible por la clase y sus subclases.
* `~` **Paquete / Interno:** Accesible por clases dentro del mismo espacio de nombres.

---

**2. Principales Relaciones entre Clases**

| Relación | Conector en Diagrama | Significado |
| --- | --- | --- |
| **Herencia** | Línea con flecha blanca `───▷` | Una clase deriva de otra (ej. *Perro* hereda de *Animal*). |
| **Asociación** | Línea continua `──────` | Relación básica entre dos clases independientes (ej. *Cliente* realiza *Pedido*). |
| **Agregación** | Línea con diamante vacío `───◇` | Relación "tiene un", donde la parte puede existir sin el todo (ej. *Universidad* tiene *Profesores*). |
| **Composición** | Línea con diamante lleno `───◆` | Relación fuerte donde la parte NO existe sin el todo (ej. *Casa* tiene *Habitaciones*). |
| **Dependencia** | Línea punteada con flecha `┈┈┈❯` | Una clase usa temporalmente a otra (ej. una clase usa una interfaz o parámetro). |

---

**3. Pasos para Crear un Diagrama de Clases**

1. **Identificar los sustantivos (Clases):** Lee los requerimientos del sistema y extrae los conceptos principales (ej. *Usuario*, *Factura*, *Producto*).
2. **Definir los atributos:** Determina qué datos necesita almacenar cada clase (ej. *Factura* necesita *fecha*, *total*).
3. **Definir los métodos:** Determina las acciones que realiza cada clase (ej. *Factura* tiene *calcularTotal()*).
4. **Establecer las relaciones y multiplicidad:** Conecta las clases indicando cuántas instancias participan en la relación (ej. `1` a `1..*` indica que un *Cliente* puede tener de 1 a muchos *Pedidos*).

---

**Ejemplo Práctico en Código C# vs UML**

Si traducimos el diagrama a código en C#:

```csharp
public class Cliente
{
    private string nombre;
    public List<Pedido> Pedidos { get; set; } = new();

    public void RealizarPedido(Pedido pedido)
    {
        Pedidos.Add(pedido);
    }
}

public class Pedido
{
    public int Id { get; set; }
    public decimal Total { get; set; }
}

```