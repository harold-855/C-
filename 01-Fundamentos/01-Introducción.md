[Inicio 🏠](../README.md) | [Siguiente ➡️](./02-Sintaxis.md)

# Que es .Net  y C#

## .Net

 Es una plataforma de desarrollo creada por Microsoft que te permite construir aplicaciónes de diversos entornos, como web, escritorio y moviles. (C# es el lenguaje diseñado para ser moderno, simple y eficiente en la creacion de aplicasiones robustas y escalable)
 
## C#

Es un lenguaje orientado a objetos que hereda caracteristicas de otros lenguajes como Java y C ++, pero que además agrega nuevas funcionalidades que lo hacen más versatil y expresivo.

### Creacion del primer proyecto:


Para nuestro primer proyecto en C# vamos a trabajarcon proyectos de consola. Lo primero que debemos hacer es abrir nuestra terminal y ejecutar el siguiente comando:

```
dotnet new console -o Miprojecto
```

#### Estructura creada:

 📁 Estructura básica de un proyecto C#

```text
MiProyecto/
│
├── 📁 bin/              → Archivos compilados de la aplicación.
├── 📁 obj/              → Archivos temporales de compilación.
├── 📄 MiProyecto.csproj → Configuración del proyecto  C#.
├── 📄 MiProyecto.sln    → Organiza uno o varios proyectos.
└── 📄 Program.cs        → Punto de entrada y código inicial.

