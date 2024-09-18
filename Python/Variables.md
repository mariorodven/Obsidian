---
dg-publish: "true"
---
Una **variable** en Python es un contenedor para almacenar datos. A diferencia de otros lenguajes de programación, Python no requiere declarar el tipo de la variable explícitamente al momento de crearla, ya que es un lenguaje de **tipado dinámico**. Sin embargo, desde **Python 3.6**, se puede usar **anotaciones de tipo** para especificar el tipo de una variable de manera explícita.

### Tipos de datos en Python

1. **Números**:
    - **int**: Números enteros (`x = 10`)
    - **float**: Números decimales (`y = 10.5`)
    - **complex**: Números complejos (`z = 3 + 4j`)
2. **Cadenas**:
    - **str**: Texto o secuencias de caracteres (`name = "Python"`)
3. **Booleanos**:
    - **bool**: Valores lógicos `True` o `False` (`is_active = True`)
4. **[[Listas]]**:
    - **list**: Colección ordenada de elementos modificables (`numbers = [1, 2, 3]`)
5. **[[Tuplas]]**:
    - **tuple**: Colección ordenada de elementos no modificables (`coordinates = (10, 20)`)
6. **[[Diccionarios]]**:
    - **dict**: Colección de pares clave-valor (`person = {"name": "John", "age": 30}`)
7. **[[Conjuntos]]**:
    - **set**: Colección de elementos únicos sin orden (`fruits = {"apple", "banana", "orange"}`)

### Declaración de Variables en Python

Para declarar una variable en Python, solo necesitas asignarle un valor con el operador de asignación ( = ):

```python
x = 10 # Variable entera 
name = "Python" # Variable cadena
```

### Especificación del Tipo con Anotaciones

A partir de Python 3.6, puedes usar **anotaciones de tipo** para indicar el tipo de una variable utilizando los dos puntos (`:`), seguido del tipo de datos y el valor de la variable:

```python
x: int = 10 # Especifica que x es un entero 
name: str = "Python" # Especifica que name es una cadena 
price: float = 19.99 # Especifica que price es un número decimal
```

### Ventajas de las Anotaciones de Tipo

- **Documentación**: Facilita la lectura del código y hace explícito qué tipo de datos se espera.
- **Ayuda al IDE**: Mejora las sugerencias y advertencias de los editores de código (como VS Code o PyCharm).

Sin embargo, Python no obliga a seguir el tipo especificado en las anotaciones, y son principalmente usadas como guía para el programador y herramientas de desarrollo.

### Ejemplo:
```python
age: int = 25 # Declara que age es un entero 
name: str = "Alice" # Declara que name es una cadena 
height: float = 1.75 # Declara que height es un número 
decimal is_student: bool = False # Declara que is_student es un booleano
```