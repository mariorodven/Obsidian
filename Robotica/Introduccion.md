### Parte 1: Introducción y Teoría (20 min)

#### ¿Qué es Arduino?

**Arduino** es una plataforma de hardware y software de código abierto utilizada para construir proyectos de electrónica interactivos. Está basada en microcontroladores que pueden ser programados para controlar una amplia variedad de dispositivos, desde sensores hasta motores. Es una herramienta versátil que permite a personas sin grandes conocimientos de electrónica o programación crear proyectos rápidamente, debido a su sencillez y accesibilidad.

#### Historia de Arduino

Arduino fue creado en 2005 por un grupo de estudiantes e ingenieros en el Instituto de Diseño Interactivo Ivrea, en Italia. Su propósito era ofrecer una alternativa económica y sencilla a otras plataformas de desarrollo. Se diseñó para estudiantes que no tuvieran experiencia previa con electrónica, lo que ayudó a democratizar el acceso al mundo de los microcontroladores.

El éxito de Arduino se debió a su enfoque en:

- **Facilidad de uso**: El entorno de programación es intuitivo y las conexiones de hardware son simples.
- **Comunidad de [[open source|código abierto]]**: Tanto el software como el hardware son de código abierto, lo que permite a desarrolladores compartir sus proyectos y colaboraciones.
- **Precio asequible**: Es más económico que otras plataformas de hardware.

#### ¿Por qué es tan popular?

Arduino es popular por su facilidad para permitir a personas de distintos niveles de habilidad experimentar con electrónica. Ofrece una forma sencilla de conectar hardware y software, además de tener una comunidad activa que comparte tutoriales, librerías y proyectos. Gracias a su bajo coste, se utiliza ampliamente en educación, makerspaces, y prototipado rápido de productos tecnológicos.

#### Comparación con otras plataformas

- **Arduino vs. Raspberry Pi**:
    - Arduino es un **microcontrolador**, diseñado principalmente para controlar dispositivos electrónicos simples. Es ideal para tareas específicas que requieren bajo consumo de energía y control de hardware.
    - Raspberry Pi, en cambio, es un **microcomputador** completo, capaz de ejecutar un sistema operativo, por lo que es más adecuado para proyectos que requieran procesamiento intensivo de datos o aplicaciones complejas (como un servidor web, procesamiento de imágenes, etc.).
- **Arduino vs. otros microcontroladores**:
    - Comparado con otros microcontroladores (como PIC o STM32), Arduino destaca por su facilidad de uso. La comunidad, el software y las librerías hacen que sea accesible, mientras que otros microcontroladores requieren un nivel más avanzado de conocimientos de electrónica y programación.

#### Modelos de Arduino

Existen varios modelos de Arduino, cada uno diseñado para satisfacer distintas necesidades de proyectos. A continuación, los modelos más comunes:

- **Arduino UNO**: El modelo más popular. Ideal para principiantes por su simplicidad y gran cantidad de ejemplos. Tiene 14 pines digitales y 6 pines analógicos, y usa el microcontrolador ATmega328P.
    
- **Arduino Nano**: Una versión más compacta que el UNO. Tiene las mismas funcionalidades, pero es mucho más pequeño, lo que lo hace ideal para proyectos donde el espacio es limitado.
    
- **Arduino Mega**: Es el modelo más grande en términos de tamaño y capacidad, con 54 pines digitales y 16 pines analógicos. Es ideal para proyectos que requieren más entradas/salidas o mayor memoria, como robots avanzados o sistemas complejos.

#### Mostrar un Arduino UNO y sus componentes básicos

El **Arduino UNO** incluye varios componentes clave:

- **Microcontrolador (ATmega328P)**: El "cerebro" de la placa, donde se almacena y ejecuta el código.
- **Pines de entrada/salida digital**: 14 pines para conectar dispositivos como LEDs, botones, motores, etc.
- **Pines de entrada analógica**: 6 pines para leer sensores analógicos como sensores de temperatura o luz.
- **Puerto USB**: Para conectar la placa a una computadora y programarla.
- **Regulador de voltaje**: Permite alimentar la placa con una fuente externa sin dañar los componentes.
- **Conector de energía**: Para alimentar la placa de manera externa usando baterías o adaptadores.

Esta sección cubre los conceptos básicos y la historia de Arduino, dándote una visión clara de por qué es una herramienta poderosa y accesible para proyectos de electrónica.

### Parte 2: Primer Programa: Blink (30 min)

#### Descripción del proyecto "Blink"

El proyecto **Blink** es el ejemplo más sencillo y clásico en Arduino. El objetivo es hacer que un LED parpadee (se encienda y apague) a intervalos regulares, lo cual introduce el concepto de **controlar salidas digitales**. Este proyecto muestra cómo encender y apagar componentes electrónicos mediante la programación de un microcontrolador.

#### Escribir el código

El código básico de Arduino sigue un formato específico que incluye dos funciones principales: `setup()` y `loop()`.

1. **`setup()`**: Esta función se ejecuta **una sola vez** al inicio del programa. Es el lugar donde configuramos los pines (entradas o salidas) y cualquier inicialización que sea necesaria para el hardware.

```c
void setup() {
  pinMode(13, OUTPUT);  // Configura el pin 13 como salida digital
}

```

2. **`loop()`**: Esta función se ejecuta **continuamente**, repitiéndose indefinidamente mientras la placa esté encendida. Aquí colocamos las instrucciones que queremos que se repitan, como hacer parpadear el LED.
   En este código, el pin 13 está configurado como una **salida** mediante la función `pinMode()`. Luego, dentro de `loop()`, se utiliza `digitalWrite()` para encender              (`HIGH`) o apagar (`LOW`) el LED, y `delay()` para esperar un tiempo en milisegundos (en este caso, 1000 ms = 1 segundo).
   
   ```c
void loop() {
  digitalWrite(13, HIGH);   // Enciende el LED
  delay(1000);              // Espera 1 segundo
  digitalWrite(13, LOW);    // Apaga el LED
  delay(1000);              // Espera 1 segundo
}
```
   
   En este código, el pin 13 está configurado como una **salida** mediante la función `pinMode()`. Luego, dentro de `loop()`, se utiliza `digitalWrite()` para encender (`HIGH`) o apagar (`LOW`) el LED, y `delay()` para esperar un tiempo en milisegundos (en este caso, 1000 ms = 1 segundo)

#### Conexión del LED

El LED se puede conectar de manera sencilla al **pin 13** de la placa Arduino (que en algunos modelos como el UNO ya tiene un LED integrado). Sin embargo, también puedes usar cualquier otro pin digital disponible, como el pin 12 o el 8. La conexión física del LED incluye:

1. **Conectar el ánodo (+)** del LED (la pata más larga) al pin 13 de la placa Arduino.
2. **Conectar el cátodo (-)** del LED (la pata más corta) a una resistencia, que luego debe conectarse a **GND** (tierra).

#### Uso de resistencias

Las resistencias son necesarias para **proteger el LED** y evitar que se queme debido a un exceso de corriente. Se suele usar una resistencia de **220Ω a 330Ω** en serie con el LED para limitar la corriente a un nivel seguro (alrededor de 20 mA). La resistencia se coloca entre el cátodo del LED y el pin GND de la placa Arduino.

Este programa introduce la base para controlar dispositivos electrónicos mediante programación y demuestra cómo la combinación de código y componentes físicos puede crear un proyecto funcional.