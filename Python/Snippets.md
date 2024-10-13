## Snippets para [[Python/Variables|Variables]] simples
1. **Convertir de int a str y viceversa**:
```python
# Convertir int a str
num = 42
num_str = str(num)
print(num_str)  # "42"

# Convertir str a int
num_from_str = int(num_str)
print(num_from_str)  # 42
```
2. **Concatenar cadenas de caracteres**:
```python
# Concatenar con +
first_name = "Juan"
last_name = "Pérez"
full_name = first_name + " " + last_name
print(full_name)  # "Juan Pérez"

# Concatenar con f-string
full_name_f = f"{first_name} {last_name}"
print(full_name_f)  # "Juan Pérez"
```
3. **Convertir de float a int (y viceversa)**:
```python
# Convertir float a int (pierde la parte decimal)
decimal = 5.75
integer = int(decimal)
print(integer)  # 5

# Convertir int a float
integer_to_float = float(integer)
print(integer_to_float)  # 5.0
```
## Snippets de [[Listas]]
1. **Crear, agregar y eliminar elementos**:
```python
# Crear una lista
fruits = ["apple", "banana", "cherry"]

# Agregar un elemento
fruits.append("orange")
print(fruits)  # ["apple", "banana", "cherry", "orange"]

# Eliminar un elemento
fruits.remove("banana")
print(fruits)  # ["apple", "cherry", "orange"]
```
2. **Acceder a elementos y hacer slicing**:
```python
# Acceder a un elemento por índice
first_fruit = fruits[0]
print(first_fruit)  # "apple"

# Slicing (obtener una sublista)
sub_list = fruits[1:3]
print(sub_list)  # ["cherry", "orange"]
```
## Snippets para [[Tuplas]]
1. **Crear y acceder a elementos**:
```python
# Crear una tupla
coordinates = (10, 20)

# Acceder a los elementos
x, y = coordinates
print(x)  # 10
print(y)  # 20
```
2. **Tuplas inmutables: no se pueden modificar**:
```python
# Las tuplas no permiten la reasignación de valores
try:
    coordinates[0] = 15
except TypeError as e:
    print("Error:", e)  # "Error: 'tuple' object does not support item assignment"

```
## [[Diccionarios]]
1. **Crear, agregar y eliminar pares clave-valor**:
```python
# Crear un diccionario
person = {"name": "Alice", "age": 30}

# Agregar un nuevo par clave-valor
person["city"] = "New York"
print(person)  # {"name": "Alice", "age": 30, "city": "New York"}

# Eliminar una clave
del person["age"]
print(person)  # {"name": "Alice", "city": "New York"}
```
2. **Acceder a valores y claves**:
```python
# Acceder al valor de una clave
name = person["name"]
print(name)  # "Alice"

# Usar get para evitar errores si la clave no existe
age = person.get("age", "Unknown")
print(age)  # "Unknown"
```
## Enum
1. **Crear un Enum y acceder a sus valores**:
```python
from enum import Enum

# Definir un Enum
class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3

# Acceder a los miembros del Enum
favorite_color = Color.RED
print(favorite_color)  # Color.RED
print(favorite_color.name)  # "RED"
print(favorite_color.value)  # 1
```
2. **Iterar sobre los miembros del Enum**:
```python
# Iterar sobre los valores del Enum
for color in Color:
    print(color.name, color.value)

# Output:
# RED 1
# GREEN 2
# BLUE 3
```