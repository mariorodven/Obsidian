## Excepciones en Python

### ¿Qué es una excepción?

Una **excepción** es un error que ocurre durante la ejecución de un programa. Cuando ocurre una excepción, el programa se detiene a menos que haya un manejo adecuado para la misma. Las excepciones son útiles porque permiten identificar y gestionar los errores sin que el programa falle de forma inesperada.

### Tipos comunes de excepciones

En Python, existen varios tipos de excepciones que pueden surgir. Algunos de los más comunes son:

- **`ZeroDivisionError`**: Ocurre cuando intentamos dividir un número por cero.
- **`TypeError`**: Ocurre cuando un tipo de dato no es el adecuado para una operación.
- **`ValueError`**: Ocurre cuando el tipo de dato es correcto, pero el valor es inválido.
- **`IndexError`**: Ocurre cuando intentamos acceder a un índice inexistente en una lista o tupla.
- **`KeyError`**: Ocurre cuando intentamos acceder a una clave que no existe en un diccionario.

### Manejo de excepciones

El manejo de excepciones en Python se realiza con la estructura **`try`** y **`except`**. Cuando ponemos un bloque de código dentro de un `try`, Python intentará ejecutarlo, pero si ocurre una excepción, saltará al bloque `except` para manejar el error.

### Ejemplo básico de manejo de excepciones

```python
try:
    # Código que puede generar una excepción
    resultado = 10 / 0
except ZeroDivisionError:
    # Lo que se hace si ocurre una división por cero
    print("Error: No se puede dividir por cero.")
```

En este ejemplo, Python intentará dividir 10 por 0, lo que generará una excepción `ZeroDivisionError`. Al detectarla, el programa entrará en el bloque `except` y mostrará el mensaje "Error: No se puede dividir por cero".

### Múltiples excepciones

Podemos manejar varios tipos de excepciones en un mismo bloque `try`, agregando diferentes bloques `except`.

```python
try:
    numero = int(input("Introduce un número: "))
    resultado = 10 / numero
except ZeroDivisionError:
    print("Error: No se puede dividir por cero.")
except ValueError:
    print("Error: Debes introducir un número válido.")
```

### El bloque `finally`

El bloque **`finally`** se ejecuta siempre, ocurra o no una excepción. Es útil para ejecutar código que debe realizarse sin importar si hubo o no un error, como cerrar archivos o liberar recursos.

```python
try:
    archivo = open("datos.txt", "r")
    contenido = archivo.read()
except FileNotFoundError:
    print("Error: El archivo no existe.")
finally:
    # Cerrar el archivo en el bloque finally
    archivo.close()
    print("El archivo ha sido cerrado.")
```

### Crear tus propias excepciones

En Python, puedes crear tus propias excepciones personalizadas. Esto es útil cuando tienes casos específicos de errores en tu programa.

```python
class MiExcepcionPersonalizada(Exception):
    pass

try:
    raise MiExcepcionPersonalizada("Este es un error personalizado.")
except MiExcepcionPersonalizada as e:
    print(f"Error: {e}")
```

### Usar `else` en el manejo de excepciones

El bloque **`else`** se ejecuta solo si no ocurre ninguna excepción en el bloque `try`.

```python
try:
    numero = int(input("Introduce un número: "))
    resultado = 10 / numero
except ZeroDivisionError:
    print("Error: No se puede dividir por cero.")
except ValueError:
    print("Error: Debes introducir un número válido.")
else:
    print(f"Resultado: {resultado}")
```

En este ejemplo, si no ocurre ningún error, el bloque `else` muestra el resultado de la división.

### Resumen

- **`try`**: Bloque que contiene el código que puede generar excepciones.
- **`except`**: Bloque donde se maneja la excepción.
- **`finally`**: Código que se ejecuta siempre, ocurra o no una excepción.
- **`else`**: Se ejecuta solo si no ocurre ninguna excepción.