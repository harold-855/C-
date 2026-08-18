[Anterior ⬅️](./03-Variables.md) | [Siguiente ➡️](./05-Formatos-de-impresion.md)

# Constante 

Una constante es similar a una variable, pero su valor no puede cambiar una vez que ha sido asignado. Las constantes se utilizan para almacenar valores que se sabe que no cambiarán durante la ejecución del programa. En C#, las constantes se definen con la palabra clave const y deben ser inicializadas en el momento de su declaración. (const (palabra clave) - C# reference, 2023) 

```
const tipo nombreConstante = valor;  
```

const double PI = 3.14159;

En este ejemplo, PI es una constante de tipo double que almacena el valor de pi, y no puede ser modificada en ningún momento durante la ejecución del programa. 

## Diferencias clave entre variables y constantes:

Variables: Su valor puede cambiar durante la ejecución del programa. 

Constantes: Su valor es inmutable después de la inicialización, lo que garantiza que no puedan ser modificadas accidentalmente. 