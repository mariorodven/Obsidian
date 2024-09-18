---
dg-publish: "true"
---
Una **tupla** en Python es una colección **ordenada** y **no mutable** (inmutable) de elementos. Al igual que las listas, las tuplas pueden contener diferentes tipos de datos, pero una vez creadas, no se pueden modificar (no se pueden añadir, eliminar o cambiar sus elementos).

### Características clave de las tuplas:

1. **Inmutabilidad**: Una vez que se crea una tupla, no se puede modificar. Esto hace que las tuplas sean más rápidas y seguras en algunos casos, ya que el contenido no se puede alterar accidentalmente.
    
2. **Ordenadas**: Al igual que las listas, las tuplas son ordenadas. Esto significa que los elementos de la tupla tienen un orden fijo y se pueden acceder mediante índices.
    
3. **Heterogéneas**: Las tuplas pueden contener diferentes tipos de datos, como enteros, cadenas, listas, e incluso otras tuplas.
    

### Declaración de tuplas

Las tuplas se declaran utilizando **paréntesis** (`()`) y los elementos están separados por comas:

```python
# Tupla de enteros
numbers = (1, 2, 3, 4, 5)

# Tupla de cadenas
fruits = ("apple", "banana", "cherry")

# Tupla mixta con diferentes tipos de datos
mixed_tuple = (1, "hello", True, 3.14)
```


```python
empty_tuple = ()
```

#### Declaración de una tupla con un solo elemento

Para declarar una tupla de un solo elemento, es necesario colocar una **coma** después del valor, ya que de lo contrario Python lo interpretará como un dato simple:

```python
single_element_tuple = (42,)  # Tupla con un solo elemento
```

### Acceso a los elementos de una tupla

Puedes acceder a los elementos de una tupla mediante su **índice**. El primer elemento tiene el índice `0`, igual que en las listas:

```python
fruits = ("apple", "banana", "cherry")

# Acceder al primer elemento
print(fruits[0])  # "apple"

# Acceder al último elemento
print(fruits[-1])  # "cherry"
```

### Recorrer una tupla

Al igual que con las listas, puedes recorrer los elementos de una tupla usando un bucle `for`:

```python
### Recorrer una tupla

Al igual que con las listas, puedes recorrer los elementos de una tupla usando un bucle `for`:
```

### Inmutabilidad de las tuplas

La inmutabilidad significa que no puedes modificar una tupla después de su creación. No puedes añadir, eliminar ni cambiar sus elementos:

```python
numbers = (1, 2, 3)

# Esto dará un error
numbers[0] = 10  # Error: 'tuple' object does not support item assignment
```

### Métodos disponibles para las tuplas

Aunque no puedes modificar una tupla, puedes usar algunos métodos para consultar información sobre ella:

1. **count()**: Devuelve cuántas veces aparece un elemento en la tupla.
```python
numbers = (1, 2, 3, 1, 1)
print(numbers.count(1))  # 3
```

2. **index()**: Devuelve el índice de la primera aparición de un elemento.
```python
fruits = ("apple", "banana", "cherry")
print(fruits.index("banana"))  # 1
```

### Convertir entre tuplas y listas

A veces es útil convertir una tupla en una lista (para modificarla) y luego volver a convertirla en tupla.

- **Convertir una tupla en lista**:
```python
fruits = ("apple", "banana", "cherry")
fruits_list = list(fruits)  # Convierte la tupla en lista
fruits_list.append("orange")  # Ahora puedes modificar la lista
```

- **Convertir una lista en tupla**:
```python
fruits_list = ["apple", "banana", "cherry"]
fruits_tuple = tuple(fruits_list)  # Convierte la lista en tupla
```

### Usos comunes de las tuplas

1. **Almacenar datos constantes**: Las tuplas son ideales para representar colecciones de datos que no deberían cambiar, como coordenadas de un punto o fechas.
```python
coordinates = (10, 20)  # Tupla para almacenar coordenadas
```

2. **Retornar múltiples valores en funciones**: Las funciones en Python pueden devolver múltiples valores empaquetándolos en una tupla.
```python
def get_person_info():
    return "John", 30, "Engineer"

name, age, profession = get_person_info()  # Desempaquetar la tupla
```

3. **Claves en diccionarios**: Dado que las tuplas son inmutables, se pueden usar como **claves** en diccionarios, mientras que las listas no pueden ser claves porque son mutables.
```python
person = ("Alice", 30, "Doctor")  # Nombre, edad y profesión agrupados en una tupla
```

4. **Agrupar datos relacionados**: Las tuplas se usan frecuentemente para agrupar varios elementos que están relacionados entre sí pero que no deberían cambiar.
```python
person = ("Alice", 30, "Doctor")  # Nombre, edad y profesión agrupados en una tupla
```

### Desempaquetado de tuplas

Puedes **desempaquetar** una tupla, es decir, asignar cada uno de sus elementos a una variable separada:

```python
person = ("Alice", 30, "Doctor")
name, age, profession = person  # Desempaqueta los elementos de la tupla
print(name)  # "Alice"
print(age)  # 30
print(profession)  # "Doctor"
```

### Conclusión

Las **tuplas** en Python son una estructura de datos fundamental que ofrece una colección ordenada e inmutable de elementos. Son útiles cuando se necesita almacenar datos que no deberían cambiar durante la ejecución del programa, como coordenadas, fechas, o valores constantes. Las tuplas ofrecen eficiencia en comparación con las listas debido a su inmutabilidad, y se usan comúnmente para retornar múltiples valores de funciones o para almacenar colecciones de datos relacionados.