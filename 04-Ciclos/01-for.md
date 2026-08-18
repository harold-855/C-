# for

El ciclo for, es una de las estructuras de control más comunes y versátiles en C#. Se utiliza cuando sabes de antemano cuántas veces necesitas repetir un bloque de código (Instrucciones de iteración: for, foreach, do y while, 2023). 

## sintaxis basica 

for (inicialización; condición; incremento/decremento) 
{ 
    // Código a ejecutar en cada iteración 
} 

ejemplo :

```
for (int i = 1; i <= 10; i++)
{
    int resultado = numero * i;
    Console.WriteLine($"{numero} x {i} = {resultado}");
}
```