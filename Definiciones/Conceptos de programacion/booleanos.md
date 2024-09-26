---
dg-publish: "true"
---
### Booleanos en Programación

Un **booleano** (o **bool**) es un tipo de dato que puede tener uno de dos valores: **`true`** (verdadero) o **`false`** (falso). Los booleanos son fundamentales en la programación porque se utilizan para controlar el flujo de los programas mediante estructuras de control como **if**, **while**, y **for**.

### Booleanos en **C**

En **C**, el tipo de dato **`bool`** fue introducido en el estándar C99 y se define en el encabezado `<stdbool.h>`. Antes de C99, los booleanos se representaban utilizando enteros (`int`), donde `0` se consideraba **falso** y cualquier valor distinto de `0` se consideraba **verdadero**.

- **`bool`** en C es una macro que se define como `int`, con los valores `true` y `false` representados como `1` y `0`, respectivamente.

#### Ejemplo en [[C]]:
```c
#include <stdbool.h>

bool es_mayor = true;
if (es_mayor) {
    printf("Es mayor.\n");
} else {
    printf("No es mayor.\n");
}
```

**Importante en C**:

- Aunque `bool` está disponible en C99 y posteriores, en versiones anteriores se usaban enteros para representar booleanos.

### Booleanos en **Rust**

En **Rust**, el tipo de dato para booleanos es **`bool`**. Los valores booleanos en Rust son **`true`** y **`false`**, y el tipo `bool` es un tipo de dato primitivo.

- **`bool`** en Rust es de tamaño fijo y ocupa un solo byte en memoria, aunque solo se necesiten 1 bit para almacenar los valores.

#### Ejemplo en Rust:
```rust
let es_mayor: bool = true;
if es_mayor {
    println!("Es mayor.");
} else {
    println!("No es mayor.");
}
```

**Importante en Rust**:

- Los booleanos en Rust son estrictos y seguros. No se permite la conversión implícita entre booleanos y otros tipos de datos.

### Booleanos en **Python**

En **Python**, el tipo de dato para booleanos es **`bool`**, y los valores son **`True`** y **`False`**. Los booleanos en Python son objetos de una clase y se comportan de manera muy flexible.

- **`bool`** en Python es un subtipo de `int`, donde `True` es equivalente a `1` y `False` es equivalente a `0`.

#### Ejemplo en Python:
```python
es_mayor = True
if es_mayor:
    print("Es mayor.")
else:
    print("No es mayor.")
```

**Importante en Python**:

- Los booleanos en Python se pueden usar en contextos donde se espera un entero, ya que `True` se evalúa como `1` y `False` como `0`.
- La conversión implícita entre booleanos y otros tipos de datos es más flexible comparado con C o Rust.

### Comparación rápida:

|Lenguaje|Tipo de Booleano|Valores|Tamaño (en memoria)|Conversión implícita|
|---|---|---|---|---|
|**C**|`bool` (C99+)|`true`, `false`|1 byte (pero es `int` en esencia)|No permitido, usar enteros|
|**Rust**|`bool`|`true`, `false`|1 byte (aunque 1 bit es suficiente)|No permitido, estricto|
|**Python**|`bool`|`True`, `False`|Variable (depende del objeto)|Permitido, `True` es `1`, `False` es `0`|

### Resumen:

- En **C**, los booleanos se representan como enteros con valores `0` para falso y no cero para verdadero. La versión moderna usa el tipo `bool` de `<stdbool.h>`.
- En **Rust**, los booleanos son un tipo de dato primitivo `bool`, que es seguro y no permite conversiones implícitas.
- En **Python**, los booleanos son objetos de la clase `bool` que se comportan de manera flexible y pueden ser utilizados en contextos numéricos.

Cada lenguaje trata los booleanos de manera diferente, pero todos los usan para controlar el flujo de programas y realizar evaluaciones lógicas.