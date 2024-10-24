## ¿Qué es la Programación Orientada a Objetos?

La **Programación Orientada a Objetos (POO)** es un paradigma de programación que organiza el código en torno a **objetos**, que son representaciones de entidades del mundo real o de conceptos abstractos. Cada objeto tiene:

1. **Atributos**: Son las características o propiedades del objeto. Se almacenan en **variables** dentro del objeto.
2. **Métodos**: Son las funciones que el objeto puede realizar, es decir, las **acciones** que puede ejecutar.

### Conceptos principales de la POO

1. **Clases**: Una **clase** es como una plantilla o modelo para crear objetos. Define los atributos y métodos que tendrán los objetos de esa clase. Por ejemplo, una clase `Coche` define cómo serán todos los coches: tendrán atributos como `color`, `marca`, y `velocidad`, y métodos como `acelerar()` y `frenar()`.

2. **Objetos**: Un **objeto** es una instancia de una clase. Si `Coche` es la plantilla, entonces un coche específico, como un coche rojo de marca Toyota, es un **objeto** de esa clase.

3. **Herencia**: La **herencia** permite crear nuevas clases a partir de clases existentes, heredando sus atributos y métodos, pero también añadiendo nuevas características o modificando las existentes.

4. **Encapsulamiento**: El **encapsulamiento** consiste en proteger los datos de un objeto para que solo puedan ser modificados a través de métodos específicos, controlando mejor el acceso y la modificación de los atributos.

5. **Polimorfismo**: El **polimorfismo** permite usar una misma interfaz para diferentes clases. Por ejemplo, diferentes tipos de animales pueden tener un método `hacerSonido()`, pero cada uno puede implementarlo de manera distinta (un perro ladra, un gato maúlla).

## Usar Programación Orientada a Objetos en Python

Python es un lenguaje que soporta la programación orientada a objetos, y te permite definir tus propias clases y objetos. Aquí tienes un ejemplo sencillo de cómo usarla:

### Ejemplo básico

```python
# Definir una clase Coche
class Coche:
    # Constructor: se ejecuta al crear un nuevo objeto
    def __init__(self, marca, color):
        self.marca = marca  # Atributo marca
        self.color = color  # Atributo color
        self.velocidad = 0  # Atributo velocidad (inicia en 0)
    
    # Método para acelerar el coche
    def acelerar(self, incremento):
        self.velocidad += incremento
        print(f"El coche {self.marca} ha acelerado. Velocidad actual: {self.velocidad} km/h")
    
    # Método para frenar el coche
    def frenar(self):
        self.velocidad = 0
        print(f"El coche {self.marca} se ha detenido.")
```

## Crear un objeto de la clase Coche

```python
# Crear un objeto llamado miCoche de la clase Coche
miCoche = Coche("Toyota", "Rojo")

# Acceder a sus atributos
print(f"Mi coche es un {miCoche.marca} de color {miCoche.color}.")

# Usar sus métodos
miCoche.acelerar(50)  # Acelerar a 50 km/h
miCoche.frenar()      # Frenar el coche
```

### Explicación del código:

1. **Clase `Coche`**: Define cómo será un coche, con atributos como `marca`, `color` y `velocidad`.
2. **Método `__init__()`**: Es el **constructor** de la clase y se ejecuta cuando creamos un nuevo objeto de la clase `Coche`. Este método inicializa los atributos.
3. **Métodos `acelerar()` y `frenar()`**: Son acciones que el coche puede realizar. El método `acelerar()` aumenta la velocidad y el método `frenar()` la reduce a 0.
4. **Crear un objeto**: La línea `miCoche = Coche("Toyota", "Rojo")` crea un nuevo objeto `miCoche` de la clase `Coche` con los atributos `marca="Toyota"` y `color="Rojo"`.

### Herencia en Python

Podemos crear una clase derivada (hija) a partir de una clase base (padre) para extender o modificar su funcionalidad. Por ejemplo, si queremos crear una clase `CocheElectrico` que herede de `Coche`:

```python
# Clase hija CocheElectrico que hereda de Coche
class CocheElectrico(Coche):
    def __init__(self, marca, color, autonomia):
        super().__init__(marca, color)  # Llama al constructor de la clase                                            padre
        self.autonomia = autonomia  # Nuevo atributo específico de                                                CocheElectrico
    
    # Nuevo método específico de los coches eléctricos
    def cargarBateria(self):
        print(f"El coche {self.marca} ha cargado la batería.")

```

Crear un objeto de la clase `CocheElectrico`

```python
miCocheElectrico = CocheElectrico("Tesla", "Blanco", 500)

# Acceder a los atributos de la clase padre e hija
print(f"Mi coche eléctrico es un {miCocheElectrico.marca} de color {miCocheElectrico.color} con {miCocheElectrico.autonomia} km de autonomía.")

# Usar métodos heredados y nuevos
miCocheElectrico.acelerar(100)
miCocheElectrico.cargarBateria()

```

Este ejemplo muestra cómo extender la funcionalidad de una clase usando la **herencia**.

### Ventajas de la POO

- **Organización**: El código está más organizado y estructurado en torno a los objetos, facilitando su mantenimiento.
- **Reutilización**: Con la herencia, puedes reutilizar y extender código existente sin duplicarlo.
- **Modularidad**: Cada clase puede desarrollarse y entenderse de forma independiente.