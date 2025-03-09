Las [[Funciones]] recursivas son una herramienta poderosa en programación que permiten resolver problemas dividiéndolos en subproblemas más pequeños del mismo tipo. En[[Introducción a la programación | Python]], una función es recursiva cuando se llama a sí misma dentro de su propio cuerpo.

## ¿Qué es la Recursión?

La recursión es una técnica en la que una función se llama a sí misma para resolver un problema. Cada llamada recursiva trabaja sobre un caso más simple hasta alcanzar una condición base que detiene la recursión.

Un problema clásico resuelto con recursión es el cálculo del factorial de un número. El factorial de un número entero positivo `n` se define como:


$$n!=n×(n−1)!n! = n \times (n-1)!$$

Con la condición base:

$$0!=10! = 1$$


Ejemplo en Python:

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # Salida: 120
```

## Componentes de una Función Recursiva

Toda función recursiva debe contar con dos partes fundamentales:

1. **Caso base**: Condición que detiene la recursión. Sin este caso, la función se llamaría indefinidamente, causando un error de desbordamiento de pila.
2. **Caso recursivo**: Llamada a la misma función con un problema más pequeño.

## Ventajas y Desventajas de la Recursión

### Ventajas:

- Facilita la solución de problemas complejos al dividirlos en partes más pequeñas.
- Hace que el código sea más legible en algunos casos, como en estructuras de datos recursivas (árboles, grafos).

### Desventajas:

- Puede ser menos eficiente que una implementación iterativa debido al uso de la pila de llamadas.
- En Python, la profundidad de recursión está limitada por defecto a 1000 llamadas (aunque puede modificarse con `sys.setrecursionlimit`).

## Ejemplo: Secuencia de Fibonacci

La secuencia de Fibonacci se define como:

$$F(n)=F(n−1)+F(n−2)F(n) = F(n-1) + F(n-2)$$

Con las condiciones base:

$$F(0)=0,F(1)=1F(0) = 0, \quad F(1) = 1$$

Implementación en Python:

```python
def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

print(fibonacci(6))  # Salida: 8
```

## Optimización de Funciones Recursivas

### 1. **Memorización (Memoization)**

Para evitar cálculos redundantes, podemos almacenar resultados ya calculados utilizando `functools.lru_cache`:

```python
from functools import lru_cache

@lru_cache(maxsize=None)
def fibonacci_memo(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci_memo(n - 1) + fibonacci_memo(n - 2)

print(fibonacci_memo(50))  # Salida: 12586269025
```

### 2. **Recursión de Cola (Tail Recursion)**

En algunos lenguajes, la recursión de cola optimiza la pila de llamadas. Python no la optimiza automáticamente, pero se puede reformular el código para evitar una pila de llamadas profunda.

```python
def factorial_tail(n, acc=1):
    if n == 0:
        return acc
    return factorial_tail(n - 1, acc * n)

print(factorial_tail(5))  # Salida: 120
```

## Conclusión

Las funciones recursivas son una herramienta poderosa para resolver problemas que pueden dividirse en subproblemas más pequeños. Sin embargo, es importante considerar el costo computacional y buscar optimizaciones como la memorización para mejorar el rendimiento.

Se recomienda utilizar la recursión cuando el problema se presta naturalmente a una solución recursiva, como estructuras de datos jerárquicas o algoritmos de backtracking, pero evitarla en casos donde una solución iterativa sea más eficiente.