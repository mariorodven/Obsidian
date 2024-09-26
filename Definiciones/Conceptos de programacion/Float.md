---
dg-publish: "true"
---
El tipo de dato **punto flotante** o **float** se utiliza para representar números que tienen parte decimal, permitiendo trabajar con valores fraccionarios. A diferencia de los enteros, los floats pueden representar números como `3.14`, `-0.001`, o `2.71828`.

### Float en **C**

En **C**, los números de punto flotante se representan utilizando los tipos de datos **`float`** y **`double`**.

- **`float`**: Generalmente ocupa 4 bytes (32 bits) y tiene una precisión de aproximadamente 6-7 dígitos decimales.
- **`double`**: Generalmente ocupa 8 bytes (64 bits) y tiene una precisión de aproximadamente 15-16 dígitos decimales.
- **`long double`**: Puede proporcionar aún más precisión dependiendo del sistema, generalmente de 12 a 16 bytes.

#### Ejemplo en C:
```C
#include <stdio.h>

int main() {
    float pi = 3.14159f;
    double e = 2.718281828459045;
    printf("Pi: %f\n", pi);
    printf("E: %lf\n", e);
    return 0;
}
```

**Importante en C**:

- La precisión y el rango de valores de los floats están limitados por el tamaño de los tipos `float` y `double`.
- Los floats pueden tener errores de redondeo debido a la precisión finita.

### Float en **Rust**

En **Rust**, los tipos de datos de punto flotante son **`f32`** y **`f64`**:

- **`f32`**: Ocupa 4 bytes (32 bits) y tiene una precisión de aproximadamente 6-7 dígitos decimales.
- **`f64`**: Ocupa 8 bytes (64 bits) y tiene una precisión de aproximadamente 15-16 dígitos decimales.

#### Ejemplo en Rust:
```rust
fn main() {
    let pi: f32 = 3.14159;
    let e: f64 = 2.718281828459045;
    println!("Pi: {}", pi);
    println!("E: {}", e);
}
```

**Importante en Rust**:

- Rust también permite operaciones matemáticas en números de punto flotante y proporciona métodos para trabajar con precisión.
- Los números flotantes en Rust también están sujetos a errores de redondeo debido a la representación finita.

### Float en **Python**

En **Python**, los números de punto flotante se representan con el tipo **`float`**. Python usa internamente **`double precision`** (64 bits) para los floats, lo que le da una precisión similar a **`double`** en C.

- **`float`** en Python es un tipo de datos de precisión doble (64 bits), que puede representar números con aproximadamente 15-17 dígitos decimales de precisión.

#### Ejemplo en Python:

```python
pi = 3.14159
e = 2.718281828459045
print(f"Pi: {pi}")
print(f"E: {e}")
```

**Importante en Python**:

- Python maneja los números de punto flotante usando precisión de doble, lo que es adecuado para la mayoría de los cálculos científicos y financieros.
- Los errores de redondeo pueden ocurrir con números flotantes debido a la representación finita.

### Comparación rápida:

|Lenguaje|Tipo de Float|Tamaño (bits)|Precisión (dígitos decimales)|Notas|
|---|---|---|---|---|
|**C**|`float`|32|6-7|`double` para mayor precisión|
|**Rust**|`f32`, `f64`|32 (f32), 64 (f64)|6-7 (f32), 15-16 (f64)|`f64` es más preciso|
|**Python**|`float`|64|15-17|Precisión de doble por defecto|

### Resumen:

- En **C**, los números flotantes pueden ser representados por `float` y `double`, con `double` proporcionando mayor precisión.
- En **Rust**, puedes usar `f32` para menor precisión y `f64` para mayor precisión, con soporte para operaciones matemáticas seguras.
- En **Python**, el tipo `float` es de precisión doble, y es simple de usar para la mayoría de las aplicaciones, aunque como todos los floats, está sujeto a errores de redondeo.

Cada lenguaje ofrece soporte para números de punto flotante con diferentes niveles de precisión y características, y es importante elegir el tipo adecuado según los requisitos de precisión y rendimiento de tu aplicación.