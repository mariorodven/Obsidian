---
dg-publish: "true"
---
Un **conjunto** en Python es una colección **desordenada** de elementos **únicos** (no hay elementos repetidos). Los conjuntos son mutables, lo que significa que se pueden modificar añadiendo o eliminando elementos. Son muy útiles cuando necesitas trabajar con colecciones sin duplicados y realizar operaciones matemáticas como **uniones** o **intersecciones**.

#### Declaración de conjuntos y operaciones básicas

Los conjuntos se definen con llaves `{}` o con la función `set()`

```python
# Declarar un conjunto
frutas = {"manzana", "banana", "naranja"}

# Añadir un elemento
frutas.add("pera")

# Eliminar un elemento
frutas.remove("banana")

# Comprobar si un elemento está en el conjunto
print("naranja" in frutas)  # True

# Operaciones matemáticas
otros_frutas = {"fresa", "manzana", "kiwi"}

# Unión: combina elementos de ambos conjuntos
union = frutas.union(otros_frutas)  # {'pera', 'naranja', 'manzana', 'fresa', 'kiwi'}

# Intersección: elementos comunes entre ambos conjuntos
interseccion = frutas.intersection(otros_frutas)  # {'manzana'}
```

#### Métodos útiles de conjuntos

- **`.add()`**: Añade un elemento al conjunto.
- **`.remove()`**: Elimina un elemento (lanza error si no existe).
- **`.union()`**: Devuelve la unión de dos conjuntos.
- **`.intersection()`**: Devuelve la intersección de dos conjuntos.

En resumen, los conjuntos son útiles para almacenar colecciones de elementos únicos y realizar operaciones matemáticas como uniones e intersecciones de forma eficiente.

