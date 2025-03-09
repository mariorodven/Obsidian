El control de flujo en Python permite dirigir la ejecución del programa en función de condiciones y repeticiones. A continuación, se explican los principales métodos de control de flujo:

## 1. Condicionales

Los condicionales permiten ejecutar diferentes bloques de código en función de una condición lógica.

### 1.1 `if`, `elif`, `else`

La estructura básica de una condición en Python es:

```python
x = 10
if x > 0:
    print("x es positivo")
elif x == 0:
    print("x es cero")
else:
    print("x es negativo")
```

- `if`: Evalúa una condición. Si es `True`, ejecuta el bloque de código.
- `elif`: Evalúa otra condición si la primera es `False`.
- `else`: Se ejecuta si ninguna de las condiciones anteriores es `True`.

### 1.2 Expresión Condicional (Operador Ternario)

Es una forma compacta de escribir una condición:

```python
x = 10
tipo = "positivo" if x > 0 else "negativo"
print(tipo)
```

---

## 2. Bucles

Los bucles permiten repetir una sección de código varias veces.

### 2.1 `for`

Se usa para iterar sobre secuencias ([[Listas]], [[Tuplas]], [[Diccionarios]], rangos, etc.).

```python
for i in range(5):
    print(i)  # Imprime números del 0 al 4
```

Ejemplo con una lista:

```python
colores = ["rojo", "verde", "azul"]
for color in colores:
    print(color)
```

### 2.2 `while`

Ejecuta un bloque de código mientras la condición sea `True`.

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

⚠️ **Cuidado con los bucles infinitos**: Asegúrate de que la condición pueda volverse `False` en algún momento.

---

## 3. Control de Bucles

### 3.1 `break`

Detiene la ejecución de un bucle antes de que finalice normalmente.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

### 3.2 `continue`

Salta la iteración actual y continúa con la siguiente.

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

### 3.3 `else` en Bucles

Un bloque `else` en un bucle `for` o `while` se ejecuta solo si el bucle termina sin que un `break` ocurra.

```python
for i in range(3):
    print(i)
else:
    print("Bucle completado sin interrupciones")
```

---

## 4. Manejo de Excepciones (`try`, `except`, `finally`)

Permite capturar y manejar errores para evitar que el programa se detenga abruptamente.

```python
try:
    x = 1 / 0  # Error de división por cero
except ZeroDivisionError:
    print("No se puede dividir entre cero")
finally:
    print("Esto se ejecuta siempre")
```

- `try`: Contiene el código que puede generar una excepción.
- `except`: Maneja la excepción si ocurre.
- `finally`: Se ejecuta siempre, haya ocurrido o no una excepción.

---

## Conclusión

Python ofrece diversas estructuras de control de flujo para gestionar la ejecución de programas de manera flexible. Es importante comprender su funcionamiento para escribir código eficiente y claro.