---
dg-publish: "true"
---
### Listas en Python

Una **lista** en Python es una colección **ordenada** y **mutable** de elementos que pueden ser de cualquier tipo de dato. Las listas son muy versátiles y se usan comúnmente para almacenar secuencias de datos.

### Características clave de las listas:

1. **Mutable**: Puedes modificar el contenido de una lista (añadir, eliminar o cambiar elementos).
2. **Indexadas**: Los elementos de una lista se acceden mediante índices, comenzando desde el índice 0.
3. **Heterogéneas**: Una lista puede contener diferentes tipos de datos, como enteros, cadenas, booleanos, e incluso otras listas.

### Declaración de listas

Para declarar una lista, se utilizan corchetes (`[]`) y los elementos de la lista están separados por comas:

```python
# Lista de números enteros 
numbers = [1, 2, 3, 4, 5] 
# Lista de cadenas 
fruits = ["apple", "banana", "cherry"] 
# Lista con diferentes tipos de datos 
mixed_list = [1, "hello", True, 3.14]
```

### Acceder a elementos de una lista

Puedes acceder a los elementos de una lista mediante su **índice**. El primer elemento tiene el índice `0`:

```python
fruits = ["apple", "banana", "cherry"]

# Acceder al primer elemento
print(fruits[0])  # "apple"

# Acceder al último elemento
print(fruits[-1])  # "cherry"
```

### Recorrer una lista

Puedes recorrer una lista usando un bucle `for`. Este es uno de los usos más comunes para iterar sobre los elementos de una lista:

```python
# Recorrer una lista de frutas
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

Si necesitas tanto el **índice** como el **valor** de cada elemento, puedes usar la función `enumerate`:

```python
# Recorrer lista con índice
for index, fruit in enumerate(fruits):
    print(f"Índice {index}: {fruit}")
```


### Métodos comunes para manipular listas

1. **Añadir elementos**:
	Usando [[Funciones]]:
    - `append()`: Agrega un elemento al final de la lista.
    - `insert()`: Inserta un elemento en un índice específico.

```python
fruits.append("orange")  # Agrega "orange" al final
fruits.insert(1, "mango")  # Inserta "mango" en la posición 1
```

2. **Eliminar elementos**:

- `remove()`: Elimina la primera aparición de un elemento específico.
- `pop()`: Elimina y devuelve el último elemento (o un elemento en un índice específico).
- `clear()`: Elimina todos los elementos de la lista.

```python
fruits.remove("banana")  # Elimina "banana"
fruits.pop()  # Elimina el último elemento
```

3. **Ordenar y revertir**:
- `sort()`: Ordena la lista en orden ascendente (puedes usar `reverse=True` para ordenar en orden descendente).
- `reverse()`: Invierte el orden de los elementos.

```python
numbers = [4, 2, 9, 1]
numbers.sort()  # Ordena en orden ascendente [1, 2, 4, 9]
numbers.reverse()  # Invierte el orden [9, 4, 2, 1]
```

4. **Buscar en la lista**:

- `index()`: Devuelve el índice de la primera aparición de un elemento.
- `in`: Comprueba si un elemento está en la lista.

```python
index_of_banana = fruits.index("banana")  # Devuelve el índice de "banana"
is_apple_in_list = "apple" in fruits  # Devuelve True si "apple" está en la lista
```

### Tipos de datos que pueden contener las listas

Las listas en Python pueden contener **cualquier tipo de dato**, incluyendo:

- **Enteros** (`int`): `[1, 2, 3]`
- **Flotantes** (`float`): `[1.5, 2.5, 3.5]`
- **Cadenas** (`str`): `["apple", "banana", "cherry"]`
- **Booleanos** (`bool`): `[True, False, True]`
- **Otras listas** (listas anidadas): `[[1, 2], [3, 4]]`
- **Objetos personalizados**: Puedes almacenar instancias de clases personalizadas en una lista.

### Usos comunes de las listas

1. **Almacenar colecciones de datos**: Las listas son útiles para almacenar secuencias de datos como nombres, edades, precios, etc.

```python
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 22]
```

2. **Procesar datos en bucles**: Las listas son ideales para iterar sobre una colección de elementos y procesarlos.
```python
for name in names:
    print(f"Hello, {name}!")
```

3. **Almacenar resultados dinámicamente**: Puedes usar listas para almacenar resultados de cálculos o procesos.
```python
squares = []
for i in range(1, 6):
    squares.append(i**2)  # Almacena los cuadrados de los números
```

4. **Listas anidadas**: Puedes usar listas dentro de listas para representar matrices o estructuras más complejas.
```python
matrix = [[1, 2], [3, 4], [5, 6]]  # Una lista de listas (matriz 3x2)
```

### Conclusión

Las **listas en Python** son una estructura de [[Variables|datos]] fundamental que permite almacenar, modificar y manipular colecciones de elementos. Son altamente flexibles y pueden contener cualquier tipo de dato, lo que las convierte en una herramienta poderosa para el desarrollo de programas que manejan secuencias de datos.