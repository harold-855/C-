# 🚀 C# — Ruta de Aprendizaje

Repositorio personal dedicado al aprendizaje de **C#**, desde los fundamentos del lenguaje hasta conceptos avanzados de programación orientada a objetos, estructuras de datos, .NET y desarrollo de aplicaciones.

> 🎯 **Objetivo:** construir una base sólida en C# mediante teoría, ejemplos prácticos, ejercicios y proyectos.

---

## 🧭 ¿Qué es C#?

**C# (C Sharp)** es un lenguaje de programación moderno, fuertemente tipado y orientado a objetos, desarrollado por Microsoft.

C# se utiliza principalmente junto con **.NET** para desarrollar diferentes tipos de aplicaciones:

- 🌐 Aplicaciones web
- 🔌 APIs y servicios backend
- 🖥️ Aplicaciones de escritorio
- 📱 Aplicaciones móviles
- 🎮 Videojuegos
- ⚙️ Servicios y aplicaciones empresariales
- ☁️ Aplicaciones y servicios en la nube

### C# vs .NET

Es importante entender que **C# y .NET no son lo mismo**:

| Concepto | Descripción |
|---|---|
| **C#** | Lenguaje de programación |
| **.NET** | Plataforma de desarrollo |
| **Rider** | Entorno de desarrollo (IDE) |
| **NuGet** | Gestor de paquetes para .NET |

Una forma sencilla de verlo:

```text
             .NET
              │
      ┌───────┴────────┐
      │                │
     C#             Bibliotecas
      │                │
      └───────┬────────┘
              │
        Aplicaciones
```

---

# 📚 Ruta de aprendizaje

El contenido está organizado progresivamente para avanzar desde los conceptos más básicos hasta temas más avanzados.

---

## 01 — Fundamentos de C#

📁 `01-Fundamentos/`

- ¿Qué es C#?
- ¿Qué es .NET?
- Estructura de un programa
- Punto de entrada
- `Main`
- Comentarios
- Variables
- Constantes
- Tipos de datos
- Inferencia de tipos
- Operadores
- Conversión de tipos
- Entrada y salida de datos
- `Console.ReadLine()`
- `Console.WriteLine()`

---

## 02 — Control de flujo

📁 `02-Control-Flujo/`

Aprenderemos a controlar el comportamiento de nuestros programas.

- `if`
- `else`
- `else if`
- `switch`
- Operador ternario
- `while`
- `do while`
- `for`
- `foreach`
- `break`
- `continue`

---

## 03 — Métodos

📁 `03-Metodos/`

Los métodos permiten dividir nuestro programa en pequeñas unidades de responsabilidad.

- Declaración de métodos
- Parámetros
- Argumentos
- Valores de retorno
- `void`
- Parámetros opcionales
- Parámetros nombrados
- Sobrecarga de métodos
- Métodos estáticos
- Expresiones lambda

---

## 04 — Estructuras de datos

📁 `04-Estructuras-Datos/`

Aprenderemos diferentes formas de almacenar y manipular información.

### Arrays

- Arrays unidimensionales
- Arrays multidimensionales
- Recorrido de arrays
- Inicialización de arrays

### Colecciones

- `List<T>`
- `Dictionary<TKey,TValue>`
- `HashSet<T>`
- `Queue<T>`
- `Stack<T>`

También aprenderemos **cuándo utilizar cada estructura**, sus características y sus ventajas y desventajas.

---

## 05 — Programación Orientada a Objetos

📁 `05-POO/`

Uno de los bloques más importantes de C#.

### Conceptos fundamentales

- Clases
- Objetos
- Propiedades
- Campos
- Métodos
- Constructores
- Encapsulamiento
- Modificadores de acceso

### Principios de POO

```text
                 POO
                  │
       ┌──────────┼──────────┐
       │          │          │
Encapsulamiento  Herencia  Polimorfismo
                  │
              Abstracción
```

---

## 06 — Clases y objetos

📁 `06-Clases-Objetos/`

Profundizaremos en la construcción de clases.

- `class`
- Objetos
- Constructores
- Propiedades
- `get`
- `set`
- Campos
- Métodos
- `this`
- `static`
- `readonly`
- Modificadores de acceso

### Ejemplo

```csharp
public class Persona
{
    public string Nombre { get; set; }
    public int Edad { get; set; }

    public void Saludar()
    {
        Console.WriteLine($"Hola, soy {Nombre}");
    }
}
```

---

## 07 — Herencia y polimorfismo

📁 `07-Herencia-Polimorfismo/`

- Herencia
- Clase base
- Clase derivada
- `protected`
- `virtual`
- `override`
- `abstract`
- Clases abstractas
- Interfaces
- Polimorfismo

---

## 08 — Interfaces y abstracción

📁 `08-Interfaces/`

- Interfaces
- Implementación
- Abstracción
- Inyección de dependencias
- Programación contra abstracciones

### Ejemplo

```csharp
public interface IAnimal
{
    void HacerSonido();
}
```

---

## 09 — Manejo de errores

📁 `09-Excepciones/`

Aprenderemos a controlar situaciones inesperadas durante la ejecución.

- Excepciones
- `try`
- `catch`
- `finally`
- `throw`
- Excepciones personalizadas
- Validación de datos

---

## 10 — Genéricos

📁 `10-Genericos/`

Los genéricos permiten crear código reutilizable y seguro respecto a tipos.

- `T`
- Métodos genéricos
- Clases genéricas
- Restricciones genéricas
- Colecciones genéricas

---

## 11 — LINQ

📁 `11-LINQ/`

**LINQ (Language Integrated Query)** permite consultar y transformar colecciones de manera expresiva.

- `Where`
- `Select`
- `OrderBy`
- `OrderByDescending`
- `First`
- `FirstOrDefault`
- `Single`
- `Any`
- `All`
- `Count`
- `Sum`
- `Average`
- `GroupBy`

### Ejemplo

```csharp
var mayores = personas
    .Where(persona => persona.Edad >= 18)
    .ToList();
```

---

## 12 — Programación asíncrona

📁 `12-Asincronia/`

- Procesamiento síncrono
- Procesamiento asíncrono
- `Task`
- `async`
- `await`
- `Task<T>`
- Operaciones concurrentes

---

## 13 — Archivos y serialización

📁 `13-Archivos/`

- Lectura de archivos
- Escritura de archivos
- Directorios
- JSON
- Serialización
- Deserialización

---

## 14 — .NET

📁 `14-DotNet/`

Aprenderemos el ecosistema que rodea a C#.

- ¿Qué es .NET?
- SDK
- Runtime
- CLI
- Proyectos `.csproj`
- Soluciones `.sln`
- NuGet
- Dependencias
- Configuración
- Estructura de proyectos

---

## 15 — Git y GitHub

📁 `15-Git-GitHub/`

Buenas prácticas para trabajar y versionar nuestros proyectos.

- Git
- Repositorios
- Commits
- Branches
- Merge
- Pull Requests
- `.gitignore`
- README
- GitHub

---

# 🧪 Ejercicios

📁 `ejercicios/`

Los ejercicios están organizados por dificultad:

```text
ejercicios/
│
├── 01-basicos/
├── 02-condicionales/
├── 03-ciclos/
├── 04-metodos/
├── 05-arrays/
├── 06-colecciones/
├── 07-POO/
├── 08-LINQ/
└── 09-proyectos/
```

La idea es **intentar resolver los ejercicios antes de consultar una solución**.

---

# 🏗️ Proyectos

📁 `proyectos/`

Los proyectos sirven para aplicar los conceptos aprendidos en situaciones más cercanas al desarrollo real.

### 🟢 Nivel básico

- Calculadora
- Conversor de unidades
- Sistema de notas
- Gestor de tareas

### 🟡 Nivel intermedio

- Sistema de inventario
- Sistema bancario
- Biblioteca
- Sistema de gestión académica

### 🔴 Nivel avanzado

- API REST
- Sistema de autenticación
- Aplicación conectada a una base de datos
- Proyecto utilizando arquitectura por capas

---

# 🧠 Metodología

La ruta sigue el siguiente ciclo:

```text
📖 TEORÍA
    ↓
💻 EJEMPLOS
    ↓
🧪 EJERCICIOS
    ↓
🏗️ PROYECTOS
    ↓
🔄 REPASO
```

La finalidad no es solamente memorizar sintaxis, sino **comprender por qué y cuándo utilizar cada herramienta**.

---

# 📈 Progreso

- [ ] Fundamentos de C#
- [ ] Variables y tipos de datos
- [ ] Operadores
- [ ] Condicionales
- [ ] Ciclos
- [ ] Métodos
- [ ] Arrays
- [ ] Colecciones
- [ ] Programación Orientada a Objetos
- [ ] Encapsulamiento
- [ ] Herencia
- [ ] Polimorfismo
- [ ] Interfaces
- [ ] Excepciones
- [ ] Genéricos
- [ ] LINQ
- [ ] Programación asíncrona
- [ ] Archivos y JSON
- [ ] .NET
- [ ] NuGet
- [ ] APIs
- [ ] Entity Framework Core
- [ ] Bases de datos
- [ ] Proyectos

---

# 🛠️ Herramientas

```text
C#
.NET
Rider
Git
GitHub
NuGet
```

---

# 🎯 Objetivo final

Al completar esta ruta, el objetivo es poder:

> **Diseñar, desarrollar, comprender y mantener aplicaciones utilizando C# y .NET, aplicando buenas prácticas de programación, estructuras de datos, programación orientada a objetos y principios de diseño de software.**

---

## 📌 Regla principal

> **No aprender C# solamente para escribir código.**
>
> **Aprender C# para aprender a resolver problemas mediante código.**

---

⭐ Este repositorio representa mi progreso y aprendizaje en C#.

**Aprender → Practicar → Equivocarse → Entender → Construir.**
