El error es que el método Console.ReadLine() no acepta texto dentro de los paréntesis. En C#, este método sirve estrictamente para leer lo que el usuario escribe, pero no puede mostrar mensajes en la pantalla al mismo tiempo. [1] 
## La solución correcta
Para pedir un dato al usuario de forma correcta, debes dividir la acción en dos pasos: primero muestras la pregunta con Console.WriteLine() y luego lees la respuesta con Console.ReadLine().
Aquí tienes el código corregido:

Console.WriteLine("¿Cuál es tu nombre?"); // 1. Muestra la preguntastring usuario = Console.ReadLine();      // 2. Lee la respuesta del teclado

## ¿Por qué da error tu código?
En lenguajes como Python, la función input("¿Cuál es tu nombre?") sí permite hacer ambas cosas a la vez. Sin embargo, en C# las funciones tienen una sola responsabilidad:

* Console.Write / WriteLine: Solo para escribir en la pantalla.
* Console.ReadLine: Solo para leer lo que el usuario escribe desde el teclado (y siempre lleva los paréntesis vacíos ()). [2, 3] 

¿Estás creando un sistema de inicio de sesión o un bot de chat? Dime qué más quieres que haga tu programa para ayudarte con las siguientes líneas.

[1] [https://www.reddit.com](https://www.reddit.com/r/csharp/comments/190vkhf/just_started_learning_c_dont_understand/?tl=es-419)
[2] [https://learn.microsoft.com](https://learn.microsoft.com/es-es/dotnet/csharp/tour-of-csharp/tutorials/hello-world)
[3] [https://www.reddit.com](https://www.reddit.com/r/csharp/comments/190vkhf/just_started_learning_c_dont_understand/?tl=es-419)
