---
dg-publish: "true"
---
### Cadenas de texto (Strings) en Programación

Un **string** o **cadena de texto** es una secuencia de caracteres. Los strings son muy utilizados en programación para almacenar y manipular texto, como palabras, frases o cualquier conjunto de caracteres. La manera en que los strings se manejan y almacenan varía entre lenguajes de programación, en términos de eficiencia, mutabilidad y soporte para caracteres especiales como **Unicode**.

### Strings en **C**

En **C**, no existe un tipo de dato nativo llamado `string`. En su lugar, las cadenas de texto se representan como **arreglos de caracteres** terminados con un **carácter nulo (`\0`)**. Esta terminación indica el fin de la cadena.

- Los strings en C se manejan como arrays de tipo `char`.
- No son **mutables** directamente (no puedes cambiar su contenido sin crear una nueva cadena o usar punteros).
- La longitud de un string en C debe ser gestionada manualmente.

#### Ejemplo en [[C]]:
```C
char saludo[] = "Hola";
printf("%s", saludo);  // Imprime: Hola
```
**Importante en C**:

- Los strings en C están delimitados por un `\0`, lo que significa que debes tener cuidado con el manejo de memoria.
- Para manipular cadenas (como concatenarlas), debes usar funciones de la biblioteca estándar como `strcpy()`, `strcat()`, etc.

### Strings en **Rust**

En **Rust**, hay dos tipos principales de cadenas: **`str`** y **`String`**.

- **`str`** es una referencia a una cadena de texto inmutable, comúnmente usada para cadenas de texto literales (por ejemplo, `&str`).
- **`String`** es un tipo de dato que permite cadenas de texto **mutables** y que pueden cambiar de tamaño dinámicamente.
- Ambas representaciones soportan **Unicode**, lo que permite manejar texto internacional.

#### Ejemplo en Rust:
```rust
let saludo = "Hola";  // Tipo &str, inmutable.
let mut saludo_mutable = String::from("Hola");  // Tipo String, mutable.
saludo_mutable.push_str(", mundo!");  // Modifica el String.
println!("{}", saludo_mutable);  // Imprime: Hola, mundo!
```

**Importante en Rust**:

- `String` es mutabilidad y puede expandirse, mientras que `&str` es inmutable y se usa para literales.
- Ambas permiten trabajar con cadenas de texto Unicode.

### Strings en **Python**

En **Python**, los strings son objetos de la clase **`str`**, y son inmutables (no puedes modificar una cadena de texto directamente, pero puedes crear una nueva cadena basada en operaciones con una existente).

- Los strings en Python son **mutables** en cuanto a la capacidad de crear nuevos objetos a partir de operaciones con otros strings, pero cada operación crea un nuevo objeto string.
- **Soporte completo para Unicode**, lo que significa que puedes trabajar con cualquier carácter o símbolo internacional.

#### Ejemplo en Python:
```python
saludo = "Hola"
saludo = saludo + ", mundo!"  # Crea una nueva cadena
print(saludo)  # Imprime: Hola, mundo!
```

**Importante en Python**:

- Los strings en Python son fáciles de manejar y permiten trabajar con Unicode de forma nativa.
- Dado que los strings son inmutables, cada vez que modifiques una cadena, estarás creando un nuevo objeto en memoria.

### Comparación rápida:

|Lenguaje|Tipo de String|Mutabilidad|Soporte de Unicode|Detalles importantes|
|---|---|---|---|---|
|**C**|Array de `char`|Mutable (pero limitado)|No (solo ASCII por defecto)|Terminado por `\0`|
|**Rust**|`String`, `&str`|`String` mutable, `&str` inmutable|Sí|`String` crece dinámicamente|
|**Python**|`str`|Inmutable|Sí|Creación de nuevas cadenas al modificar|

### Resumen:

- En **C**, los strings son arrays de caracteres terminados por `\0` y deben manejarse con cuidado para evitar errores de memoria.
- En **Rust**, tienes tanto cadenas inmutables (`&str`) como mutables (`String`), y ambas soportan Unicode, haciéndolo flexible para aplicaciones modernas.
- En **Python**, los strings son inmutables pero altamente manejables. Puedes realizar operaciones fácilmente y trabajar con texto Unicode sin preocuparte por los detalles de codificación o tamaño.

Cada lenguaje ofrece un enfoque diferente para trabajar con strings: C es más bajo nivel, Rust proporciona seguridad y flexibilidad con Unicode, y Python es extremadamente fácil de usar para manipular texto.