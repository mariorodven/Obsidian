---
dg-publish: "true"
---
Un **carácter** o **char** es un tipo de dato que representa un único símbolo, como una letra, un número o un signo de puntuación. Los caracteres se almacenan utilizando estándares como **ASCII** (7 bits) o **Unicode** (generalmente más grande, permite representar casi todos los símbolos y letras del mundo).

Los caracteres son tratados de manera diferente según el lenguaje de programación, en términos de tamaño y codificación. Vamos a ver cómo se manejan los caracteres en **C**, **Rust**, y **Python**.

### Caracteres en **[[C]]**

En **C**, el tipo de dato para un carácter es **`char`**, y ocupa **1 byte** (8 bits), lo que significa que puede representar **256 valores diferentes** (valores entre -128 y 127 en signed `char`, o 0 a 255 en unsigned `char`).

- Los caracteres están codificados en **ASCII** por defecto, lo que significa que cada número entre 0 y 127 corresponde a un símbolo o letra.
- Se almacenan entre comillas simples (`'a'`, `'b'`).

#### Ejemplo en C:

```C
char letra = 'A';
```

- **Importante**: Un `char` en C es esencialmente un entero de 8 bits, por lo que se puede realizar operaciones aritméticas con él.
### Caracteres en **Rust**

En **Rust**, los caracteres están representados por el tipo **`char`**, pero, a diferencia de C, un `char` en Rust representa **cualquier carácter Unicode** y ocupa **4 bytes** (32 bits). Esto significa que puede almacenar caracteres de muchos alfabetos y símbolos.

- Se almacenan entre comillas simples (`'a'`, `'€'`).

#### Ejemplo en Rust:

```rust
let letra: char = 'A';
let simbolo: char = '€';  // Admite Unicode.
```

- **Importante**: Los `char` en Rust pueden representar cualquier carácter Unicode, lo que los hace más flexibles que en C, pero ocupan más memoria.

### Caracteres en **[[Introducción a la programación|Python]]**

En **Python**, no existe un tipo específico para **caracteres individuales** como en C o Rust. En su lugar, Python trata los **caracteres como cadenas de un solo carácter**. Las cadenas (`str`) en Python son secuencias de **Unicode**, lo que permite representar cualquier símbolo o carácter del mundo.

- Se almacenan entre comillas simples o dobles (`'a'`, `"b"`, `'€'`).

#### Ejemplo en Python:

```python
letra = 'A'
simbolo = '€'  # Python maneja Unicode de forma nativa.
```

- **Importante**: En Python, los caracteres se manejan como cadenas de un solo carácter. Dado que Python utiliza Unicode de forma predeterminada, puedes trabajar fácilmente con caracteres de cualquier idioma o símbolo especial.
### Comparación rápida:

| Lenguaje   | Tipo de Carácter | Tamaño (bits) | Soporte de Unicode |
| ---------- | ---------------- | ------------- | ------------------ |
| **C**      | `char`           | 8             | No, solo ASCII     |
| **Rust**   | `char`           | 32            | Sí, completamente  |
| **Python** | `str` (1 char)   | Dinámico      | Sí, completamente  |

### Resumen:

- En **C**, un carácter ocupa 1 byte y está limitado a los símbolos representados en ASCII.
- En **Rust**, los caracteres son de 4 bytes y soportan cualquier carácter Unicode.
- En **Python**, los caracteres son realmente cadenas Unicode de longitud 1, lo que ofrece flexibilidad y soporte para cualquier símbolo global, aunque sin un tipo de dato explícito para caracteres individuales.

En términos de uso, **C** es más eficiente en memoria para caracteres simples, mientras que **Rust** y **Python** son más flexibles al manejar caracteres complejos o internacionales debido a su soporte para **Unicode**.