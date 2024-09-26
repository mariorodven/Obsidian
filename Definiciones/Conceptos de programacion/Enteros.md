---
dg-publish: "true"
---
Un **entero** o **int** es un tipo de dato que representa números enteros, es decir, sin decimales. Los enteros pueden ser **positivos** o **negativos**. La forma en que los enteros se manejan y almacenan varía entre diferentes lenguajes de programación, y los tamaños (o rangos) de enteros pueden depender del lenguaje y del sistema operativo.

### Enteros en **[[C]]**

En **C**, los enteros tienen un tamaño fijo y hay diferentes tipos de enteros con distintos rangos. El tamaño de los enteros depende del compilador y la arquitectura, pero en general, los tipos comunes son:

- **`int`**: Generalmente de 4 bytes (32 bits), con un rango de -2,147,483,648 a 2,147,483,647.
- **`short`**: Menor que un `int`, típicamente de 2 bytes (16 bits).
- **`long`**: Mayor que un `int`, generalmente de 4 u 8 bytes, dependiendo del sistema.
- **`long long`**: Típicamente de 8 bytes (64 bits).

#### Ejemplo en C:
```c
int a = 42;
long b = 1234567890;
```

### Enteros en **Rust**

En **Rust**, los tipos de enteros son más explícitos, y se especifican tanto el tamaño como el signo (positivo o negativo). Los tipos de enteros incluyen:

- **`i8`**, **`i16`**, **`i32`**, **`i64`**, **`i128`**: Enteros con signo, donde el número indica el número de bits.
- **`u8`**, **`u16`**, **`u32`**, **`u64`**, **`u128`**: Enteros sin signo (solo positivos).

El tamaño de los enteros es estrictamente controlado, lo que evita el uso inesperado de memoria.

#### Ejemplo en Rust:
```rust
let x: i32 = 42;
let y: u64 = 1234567890;
```

### Enteros en **[[Introducción a la programación|Python]]**

En **Python**, los enteros (`int`) no tienen un tamaño fijo, lo que significa que puedes trabajar con números extremadamente grandes sin preocuparte por desbordamientos. Python ajusta automáticamente el tamaño del entero según sea necesario. En Python 2, había una diferencia entre `int` y `long`, pero en Python 3, todos los enteros son de tipo **`int`** y pueden crecer indefinidamente.

#### Ejemplo en Python:
```python
x = 42
y = 12345678901234567890  # Python maneja grandes enteros sin problemas.
```

#### **Cosas importantes a tener en cuenta en Python**:

- Los **enteros en Python** pueden crecer en tamaño automáticamente si se necesita, lo que no ocurre en lenguajes como C o Rust.
- No necesitas preocuparte por **long int** en Python 3, ya que todo `int` puede almacenar números muy grandes sin declarar un tipo especial.

### Comparación rápida:

|Lenguaje|Tipo de Entero|Tamaño (bits)|Rango|
|---|---|---|---|
|**C**|`int`|32|-2³¹ a 2³¹-1|
|**Rust**|`i32`, `u32`|32|Depende del signo|
|**Python**|`int`|Dinámico|Ilimitado (en la práctica, limitado por la memoria)|

En resumen, mientras que lenguajes como **C** y **Rust** tienen tamaños fijos para enteros, lo que puede llevar a **desbordamientos**, en **Python** los enteros crecen dinámicamente según lo necesites, lo que lo hace más seguro en cuanto a manejar números grandes, pero posiblemente más lento en rendimiento.