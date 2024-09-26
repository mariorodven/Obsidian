En el lenguaje de programación C, las [[Python/Variables|Variables]] son una forma de almacenar datos en memoria, y existen varios tipos de variables que pueden representar distintos tipos de datos. A continuación, te explico los principales tipos de variables en C:

### 1. **Tipos básicos o primitivos**

Estos son los tipos de datos fundamentales de C:

- **`int`**: Almacena números enteros (positivos o negativos) sin decimales. El tamaño de un `int` depende de la arquitectura del sistema, pero generalmente es de 4 bytes.
- **`float`**: Almacena números en coma flotante, es decir, números con decimales, de precisión simple (4 bytes).
- **`double`**: Almacena números en coma flotante de doble precisión (8 bytes), lo que permite una mayor precisión en cálculos con decimales.
- **`char`**: Almacena un solo carácter (1 byte). Puede almacenar cualquier valor que represente un carácter ASCII.

```c
int edad = 25;
float temperatura = 36.5;
double pi = 3.1415926535;
char inicial = 'A';
```

### 2. **Tipos modificados**

C permite modificar el tamaño y el comportamiento de los tipos básicos mediante ciertos modificadores, como `signed`, `unsigned`, `short` y `long`:

- **`unsigned`**: Hace que la variable solo pueda almacenar números positivos (o cero). Como resultado, el rango de los números posibles se extiende en el lado positivo.
- **`signed`**: Es el valor por defecto para los enteros y permite almacenar números tanto positivos como negativos. Aunque generalmente no es necesario escribir `signed`, puedes hacerlo explícitamente si lo prefieres.
- **`short`**: Se utiliza para declarar variables de enteros pequeños, generalmente de 2 bytes. Esto es útil cuando sabes que los valores no serán muy grandes.
- **`long`**: Se utiliza para declarar enteros grandes. Generalmente ocupa 4 u 8 bytes, dependiendo de la arquitectura.
- También existe **`long long`**, que garantiza que la variable tenga al menos 8 bytes de almacenamiento.

```c
unsigned int cantidad = 300;
signed int saldo = -50;
short int pequenoNumero = 32767;
long int grande = 1234567890;
```

### 3. **Tipos de almacenamiento**

En C, hay varias formas de especificar la duración de una variable en la memoria y su alcance (dónde es accesible). Estas características están controladas por las "clases de almacenamiento":

- **`auto`**: Es el tipo predeterminado de almacenamiento para variables locales. Su vida útil se limita al bloque de código en el que son declaradas, y no es necesario escribir la palabra clave `auto`, ya que es el comportamiento predeterminado.
- **`static`**: Hace que la variable conserve su valor entre llamadas a la misma función. También limita el alcance de una variable global a solo el archivo donde fue declarada.
- **`extern`**: Se utiliza para declarar una variable que está definida en otro archivo o en otro lugar del programa. Esto permite compartir variables entre distintos archivos de código.
- **`register`**: Solicita al compilador que almacene la variable en un registro de la CPU para mejorar la velocidad de acceso (aunque esto depende del compilador y no es garantizado).

```c
auto int x = 10;  // Equivalente a solo "int x = 10;"
static int contador = 0;
extern int contadorGlobal;
register int rapido = 5;
```

### 4. **Punteros**

Los punteros son variables que almacenan la dirección de memoria de otra variable. Son fundamentales para el manejo dinámico de la memoria y manipulación directa de datos.

- **`int*`**: Declara un puntero a un entero.
- **`char*`**: Declara un puntero a un carácter.

```c
int* ptr;
char* nombre;
```

### 5. **Tipos derivados**

Además de los tipos básicos, C tiene varios tipos derivados:

- **Arrays**: Un conjunto de elementos del mismo tipo.
- **Structs**: Estructuras que agrupan diferentes tipos de datos bajo un mismo nombre.
- **Unions**: Similar a una estructura, pero en lugar de almacenar todos los miembros por separado, un `union` utiliza el mismo espacio de memoria para todos sus miembros.

```c
int numeros[5] = {1, 2, 3, 4, 5};
struct Persona {
    char nombre[50];
    int edad;
};
union Valores {
    int entero;
    float flotante;
};
```

### Resumen

Los tipos de variables en C incluyen desde enteros simples (`int`, `unsigned`, `long`) hasta variables de coma flotante (`float`, `double`) y caracteres (`char`). A través de modificadores y tipos derivados como `struct` y `union`, C permite una gran flexibilidad y control sobre la memoria, lo cual es clave para desarrollar aplicaciones eficientes y de bajo nivel.