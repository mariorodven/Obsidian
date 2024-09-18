---
dg-publish: "true"
---
Un **diccionario** en Python es una colección **desordenada** de pares **clave-valor**. Cada clave es única y se utiliza para acceder a su valor asociado. Los diccionarios son mutables, lo que significa que puedes modificar sus valores, añadir o eliminar elementos.

#### Declaración de diccionario y acceso a elementos

Los diccionarios se definen con llaves `{}`, y los pares clave-valor se separan por comas, con los valores asociados a claves mediante el operador `:`

```python
# Declarar un diccionario
persona = {
    "nombre": "Alice",
    "edad": 30,
    "profesion": "Ingeniera",
}

# Acceder a un valor mediante su clave
print(persona["nombre"])  # Alice

# Modificar un valor
persona["edad"] = 31

# Añadir un nuevo par clave-valor
persona["ciudad"] = "Madrid"

# Eliminar un elemento
del persona["profesion"]
```

#### Métodos útiles de diccionarios

Algunos métodos comunes incluyen:

- **`.keys()`**: Devuelve las claves del diccionario.
- **`.values()`**: Devuelve los valores del diccionario.
- **`.items()`**: Devuelve los pares clave-valor como tuplas.

```python
for clave, valor in persona.items():
    print(f"{clave}: {valor}")
```

En resumen, los diccionarios son útiles para almacenar datos relacionados y permiten acceder rápidamente a los valores mediante sus claves.