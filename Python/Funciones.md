---
dg-publish: "true"
---
Una **función** es un bloque de código reutilizable que realiza una tarea específica. Las funciones en Python permiten dividir un programa en partes más pequeñas y manejables, facilitando el mantenimiento y la reutilización del código.

### Declarar una función

En Python, las funciones se definen utilizando la palabra clave `def`, seguida del **nombre de la función**, los **parámetros** entre paréntesis, y dos puntos (`:`). El bloque de código dentro de la función debe estar indentado.

```python
def nombre_funcion():
    # Bloque de código
    print("Hola, esta es una función")
```

Ejemplo simple:

```python
def saludar():
    print("Hola, bienvenido!")

#Y para llamarla
saludar()
```


### Argumentos y parámetros

Las funciones pueden aceptar **[[Python/Variables|argumentos]]**, que son valores que se pasan a la función para que ésta los utilice en su ejecución.

#### Función con un argumento:

```python
def saludar(nombre):
    print(f"Hola, {nombre}!")

saludar("Alice")                                    # Salida: Hola, Alice!
```

Función con varios argumentos:

```python
def sumar(a, b):
    return a + b


resultado = sumar(3, 4)  # Salida: 7
```

### Tipos de argumentos

1. **Argumentos por posición**: Se pasan en el orden en el que están definidos en la función.

```python
def mostrar_datos(nombre, edad):
    print(f"Nombre: {nombre}, Edad: {edad}")

mostrar_datos("Juan", 25)  # Nombre: Juan, Edad: 25
```

2. **Argumentos por nombre (keyword arguments)**: Se especifican por nombre, no importa el orden en el que se pasen.

```python
mostrar_datos(edad=30, nombre="Carlos")  # Nombre: Carlos, Edad: 30
```

3. **Valores por defecto**: Puedes asignar valores por defecto a los parámetros. Si no se proporciona un valor, se usará el valor por defecto.

```python
def saludar(nombre="Mundo"):
    print(f"Hola, {nombre}!")

saludar()  # Hola, Mundo!
saludar("Alice")  # Hola, Alice!
```

4. **Argumentos variables**:

- **`*args`**: Permite pasar una cantidad indefinida de argumentos posicionales a una función.
```python
def sumar(*numeros):
    return sum(numeros)

print(sumar(1, 2, 3, 4))  # 10

```

- **`**kwargs`**: Permite pasar una cantidad indefinida de argumentos por nombre.
```python
def mostrar_informacion(**datos):
    for clave, valor in datos.items():
        print(f"{clave}: {valor}")

mostrar_informacion(nombre="Alice", edad=30, profesion="Ingeniera")
```

### Retorno de valores

Las funciones pueden **retornar** valores usando la palabra clave `return`. Una vez que se ejecuta `return`, la función termina.

```python
def multiplicar(a, b):
    return a * b

resultado = multiplicar(5, 3)  # 15
```

### Funciones de la biblioteca estándar

Python incluye una gran cantidad de **funciones integradas** que están disponibles sin necesidad de importarlas. Algunas funciones comunes de la biblioteca estándar incluyen:

- **`len()`**: Devuelve la longitud de un objeto, como una lista o cadena.
- **`max()` y `min()`**: Devuelven el valor máximo o mínimo de una secuencia.
- **`sum()`**: Suma todos los elementos de una lista.
- **`range()`**: Genera una secuencia de números enteros.
- **`abs()`**: Devuelve el valor absoluto de un número.
- **`type()`**: Devuelve el tipo de una variable.
```python
longitud = len("Hola")  # 4
mayor = max([1, 2, 3, 4]) # 4
total = sum([1, 2, 3, 4]) # 10
for i in range(5):
    print(i)
valor = abs(-10)  # 10
tipo = type(10)  # <class 'int'>
```

### Funciones Lambda (funciones anónimas)

Las **funciones lambda** son funciones pequeñas y anónimas que pueden definirse en una sola línea. Se suelen usar para tareas simples.

```python
# Función lambda para sumar dos números
sumar = lambda a, b: a + b

print(sumar(3, 5))  # 8
```

### Funciones como objetos de primera clase

En Python, las funciones son **objetos de primera clase**, lo que significa que puedes pasarlas como argumentos a otras funciones, almacenarlas en variables, o retornarlas desde otras funciones.

Pasar una función como argumento:

```python
def aplicar_operacion(funcion, a, b):
    return funcion(a, b)

resultado = aplicar_operacion(sumar, 4, 5)  # Usa la función sumar
print(resultado)  # 9
```

### Usos de las funciones

1. **Reutilización de código**: Permiten ejecutar un mismo bloque de código múltiples veces sin tener que reescribirlo.
2. **Modularidad**: Facilitan la organización del código en bloques más pequeños y manejables.
3. **Facilitar el mantenimiento**: Si se necesita realizar un cambio en el comportamiento de un bloque de código, solo se necesita modificar la función.

### Conclusión

Las funciones son una de las herramientas más poderosas y útiles en Python, permitiendo organizar y reutilizar el código. Las funciones pueden recibir argumentos, devolver valores y se pueden utilizar con diversas técnicas como argumentos variables, valores por defecto, o funciones anónimas (lambda). Además, las funciones integradas de la biblioteca estándar ofrecen soluciones rápidas para tareas comunes.