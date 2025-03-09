## Entradas y salidas digitales

- Entradas digitales
- Salidas digitales
- Ejemplo
- Ejemplo practico

## Entradas digitales
 ## *¿Qué es una entrada digital?*
  Una **señal digital** es una variación de voltaje entre `-Vcc` y `+Vcc`, sin pasar por valores intermedios (por ejemplo, `0V` y `5V`). Por lo tanto, una señal digital solo dispone de **dos estados**: 
   - Al valor **inferior** (`-Vcc`), le asociamos un valor lógico **`LOW`** (`0` lógico).
   - Al valor **superior** (`+Vcc`), le asociamos un valor lógico **`HIGH`** (`1` lógico).
 ## *Diseño de dos objetos con tabla*
 ## ¿Cómo funciona una entrada digital en el ESP-12S?

En realidad, las señales de **tensión** son **continuas**. No existe una señal que cambie instantáneamente de un valor de tensión a otro sin pasar por valores intermedios.  

El proceso de lectura digital se basa en un proceso de **discretización**, donde convertimos una medida analógica (el valor real de la tensión) en una señal digital **idealizada**.  

### ¿Cómo se realiza la conversión de analógico a digital?

Una **entrada digital** compara la medida real de la tensión con un **valor umbral** predefinido.  
- Si el **valor medido** es **superior** a la tensión umbral, la entrada digital devuelve **`HIGH`** (`1` lógico).  
- Si el **valor medido** es **inferior** a la tensión umbral, devuelve **`LOW`** (`0` lógico).  
![[senal.png]]
### Niveles lógicos en el ESP-12S  
El **ESP-12S** opera con una lógica de **3.3V**, por lo que los niveles de tensión son los siguientes:  

- **`LOW (0 lógico)`** → Si la señal de entrada está **por debajo de 0.8V**.  
- **`HIGH (1 lógico)`** → Si la señal de entrada está **por encima de 2.4V**.  
- Entre estos valores, el estado es **indeterminado**, lo que puede causar lecturas erróneas.  

### Consideraciones importantes en el ESP-12S  
🔹 **Ruido en la señal**: Pequeñas variaciones pueden provocar cambios inesperados en la lectura digital. Se recomienda usar **resistencias pull-up o pull-down** para mantener un estado definido cuando la entrada no está conectada.  
🔹 **Entradas flotantes**: Si un pin de entrada digital no está conectado, puede quedar en un estado inestable y cambiar de valor aleatoriamente.  
🔹 **GPIOs en el arranque**: Algunos pines del ESP-12S tienen estados específicos al inicio, lo que puede interferir con el uso de ciertas entradas digitales.  

En resumen, en el **ESP-12S**, una entrada digital no mide una señal perfectamente binaria, sino que la **interpreta** a partir de una comparación con un umbral de tensión. 

### Entradas digitales en ESP32
En ESP32 las entradas y salidas digitales comparten PIN. Por este motivo se denominan I/O digitales **(input / output)**.
Esto significa que el mismo pin puede ejecutar funciones tanto de entrada como de salida aunque, lógicamente, **no de forma simultánea**. Es necesario configurar un pin I/O como entrada o salida.
Los valores de alimentación habituales en las ESP32 son 0V y 3’3V. En este caso la tensión umbral será muy cercana a 1’65V. Por tanto:
- Si medimos una tensión con un valor intermedio entre 0 a 1’65V devolverá una lectura `LOW`
	- Si medimos un valor entre 1’65V y 3’3V, devolverá `HIGH`.

### Declarar entradas digitales

En Arduino para tratar las entradas y salidas digitales usamos las siguientes funciones:
-  `pinMode()` –> configura en el pin si se va a comportar como una entrada o una salida.
- `digitalRead()` –> lee el valor del pin correspondiente como `HIGH` o `LOW`. Por defecto los digital I/O pins están configurados como inputs y no hace falta llamar a la función `pinMode()` aunque es recomendable para aclarar el código.

## Salidas digitales
Recordaremos que una señal digital puede variar únicamente entre dos valores, que denominamos -Vcc y +Vcc. Una salida digital es un dispositivo que permite variar su tensión a uno de estos dos valores. Por tanto, podemos usarlas para realizar acciones con el entorno. En Arduino, en general, los voltajes -Vcc y +Vcc corresponden con 0V (GND) y 5V.

![[salidas digitales.png]]

