# Conceptos

* **Clases:** Son como planos o plantillas que definen las propiedades y métodos que tendrá un objeto.
* **Objetos:** Son instancias de una clase. A partir de una clase, puedes crear múltiples objetos con diferentes valores en sus propiedades.
* **Propiedades:** Son las características de un objeto. Por ejemplo, el nombre de un personaje o el color de un coche.
* **Métodos:** Son las acciones que un objeto puede realizar, como atacar en un videojuego o acelerar en el caso de un coche.
* **Encapsulamiento:** Permite proteger los datos de un objeto, asegurando que solo se puedan acceder o modificar a través de métodos definidos.
* **Herencia:** Facilita la reutilización del código, permitiendo que una clase herede propiedades y métodos de otra clase.
* **Polimorfismo:** Es la capacidad de los objetos para comportarse de diferentes maneras, dependiendo del contexto en el que se utilicen.
* **Abstracción:** Consiste en simplificar la complejidad al enfocarse en los aspectos más relevantes de un objeto, ocultando los detalles innecesarios.

## Los modificadores de acceso 

En C# definen la visibilidad y el alcance de las clases, métodos, propiedades y otros miembros dentro de un programa.

public: El acceso no está restringido. El miembro o clase puede ser visto y utilizado desde cualquier parte de la solución o ensamblado externo.

private: El acceso está restringido exclusivamente a la clase o estructura donde se declara. No es accesible desde clases derivadas ni desde fuera.

protected: El miembro solo es accesible dentro de su propia clase y por las clases que heredan de ella (clases derivadas).

internal: El miembro o clase es accesible desde cualquier parte del mismo proyecto o ensamblado (.dll o .exe), pero no desde proyectos externos.