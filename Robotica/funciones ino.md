Las funciones en Arduino permiten organizar y reutilizar código para hacer que los programas sean más legibles y modulares. En el entorno de desarrollo de Arduino, las funciones se utilizan para dividir el código en bloques reutilizables.

## ¿Qué es una Función?

Una función es un bloque de código que realiza una tarea específica. En Arduino, todas las funciones deben estar definidas antes de su uso o declaradas previamente si están después del `loop()` y `setup()`.

## Estructura de una Función en Arduino

Una función en Arduino tiene la siguiente estructura:

```cpp
tipo_de_retorno nombre_de_funcion(parámetros) {
    // Código de la función
    return valor; // (Opcional, si el tipo de retorno no es 'void')
}
```

### Ejemplo:

```cpp
int suma(int a, int b) {
    return a + b;
}

void setup() {
    Serial.begin(9600);
    int resultado = suma(5, 3);
    Serial.println(resultado);  // Salida: 8
}

void loop() {
    // Código principal en ejecución continua
}
```

## Tipos de Funciones en Arduino

### 1. **Funciones sin Retorno (`void`)**

Las funciones `void` no devuelven ningún valor, solo ejecutan instrucciones.

```cpp
void parpadearLED(int pin, int tiempo) {
    digitalWrite(pin, HIGH);
    delay(tiempo);
    digitalWrite(pin, LOW);
    delay(tiempo);
}

void setup() {
    pinMode(13, OUTPUT);
}

void loop() {
    parpadearLED(13, 500); // Parpadeo cada 500 ms
}
```

### 2. **Funciones con Retorno**

Las funciones pueden devolver un [[C/Variables|valor]] de tipo `int`, `float`, `char`, `boolean`, etc.

```cpp
float convertirCelsiusAFahrenheit(float celsius) {
    return (celsius * 9.0 / 5.0) + 32.0;
}

void setup() {
    Serial.begin(9600);
    float tempF = convertirCelsiusAFahrenheit(25);
    Serial.println(tempF);  // Salida: 77.0
}

void loop() {}
```

### 3. **Funciones con Parámetros**

Las funciones pueden recibir parámetros para hacerlas más dinámicas y reutilizables.

```cpp
void encenderLED(int pin, int tiempo) {
    digitalWrite(pin, HIGH);
    delay(tiempo);
    digitalWrite(pin, LOW);
}

void setup() {
    pinMode(8, OUTPUT);
}

void loop() {
    encenderLED(8, 1000);  // Enciende por 1 segundo
    delay(1000);
}
```

## Funciones Especiales en Arduino

### 1. `setup()`

Se ejecuta una sola vez al inicio del programa. Se usa para configurar pines, inicializar seriales, etc.

```cpp
void setup() {
    Serial.begin(9600);
    pinMode(13, OUTPUT);
}
```

### 2. `loop()`

Se ejecuta en bucle infinito después de `setup()`.

```cpp
void loop() {
    Serial.println("Ejecutando loop");
    delay(1000);
}
```

## Conclusión

Las funciones en Arduino son fundamentales para organizar y modularizar el código, permitiendo reutilizar lógica y mejorar la legibilidad. Al utilizar funciones adecuadamente, se pueden crear programas más eficientes y fáciles de mantener.