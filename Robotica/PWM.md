## ¿Qué es una señal PWM?

PWM, o **Modulación por Ancho de Pulso** (del inglés *Pulse Width Modulation*), es una técnica utilizada para controlar la cantidad de energía que se suministra a un dispositivo electrónico, mediante la variación del ciclo de trabajo de una señal digital.

### Concepto básico
Una señal PWM es una señal digital que alterna entre estados de **encendido (HIGH)** y **apagado (LOW)** en una frecuencia fija. Lo que varía es la proporción de tiempo que la señal permanece en estado HIGH durante cada ciclo completo de la señal. A esta proporción se le llama **ciclo de trabajo** o *duty cycle*, y se expresa como un porcentaje.

- **Ciclo de trabajo** del 0%: La señal está siempre en estado LOW (apagada).
- **Ciclo de trabajo** del 50%: La señal está encendida el 50% del tiempo y apagada el otro 50% (una señal cuadrada perfecta).
- **Ciclo de trabajo** del 100%: La señal está siempre en estado HIGH (encendida).

### Frecuencia y ciclo de trabajo
- **Frecuencia**: Es la velocidad a la que la señal alterna entre los estados HIGH y LOW. Se mide en Hz (hercios), que indica cuántos ciclos ocurren por segundo.
- **Duty cycle (ciclo de trabajo)**: Es el porcentaje del tiempo en que la señal permanece en estado HIGH dentro de un ciclo.

Por ejemplo, si se tiene una señal PWM con una frecuencia de 1 kHz (1000 ciclos por segundo) y un ciclo de trabajo del 25%, la señal estará encendida (HIGH) durante el 25% del tiempo de cada ciclo y apagada (LOW) durante el 75%.

### Aplicaciones de la señal PWM
La modulación por ancho de pulso se utiliza en muchas aplicaciones en las que necesitamos controlar dispositivos de manera eficiente, ya que permite regular la potencia sin perder energía en forma de calor, a diferencia de los métodos de control lineal. Algunos ejemplos de uso incluyen:

- **Control de velocidad de motores DC**: Mediante la modulación del ciclo de trabajo, se puede controlar la velocidad del motor de forma eficiente.
- **Control de brillo de LEDs**: Variando el ciclo de trabajo, se puede ajustar la intensidad del brillo del LED sin afectar el color o la eficiencia energética.
- **Generación de tonos**: Los altavoces pueden ser controlados usando señales PWM para generar sonidos de diferentes frecuencias.
  
### PWM en Arduino
En Arduino, puedes generar señales PWM usando la función `analogWrite(pin, value)`, donde `pin` es el número del pin que admite PWM y `value` es un valor entre 0 y 255 que determina el ciclo de trabajo (0 = 0%, 255 = 100%).

Ejemplo de código en Arduino:
```cpp
int pinPWM = 9;  // Pin que admite PWM

void setup() {
  pinMode(pinPWM, OUTPUT);  // Configuramos el pin como salida
}

void loop() {
  analogWrite(pinPWM, 128);  // Envía una señal PWM con un ciclo de trabajo del 50%
  delay(1000);               // Espera un segundo
}
```

En este ejemplo, un valor de 128 genera un ciclo de trabajo del 50%, lo que significa que la señal estará encendida la mitad del tiempo y apagada la otra mitad.

### Beneficios del uso de PWM

- **Eficiencia energética**: Al estar controlando la energía mediante el encendido y apagado de la señal, se evita la disipación de calor en resistencias o controladores lineales.
- **Control preciso**: Permite un control preciso sobre la cantidad de energía suministrada a un dispositivo, como la velocidad de un motor o el brillo de un LED.

## Elementos electrónicos que usan la señal PWM

La señal PWM (Modulación por Ancho de Pulso) se utiliza en una amplia variedad de dispositivos electrónicos para controlar diferentes parámetros, como velocidad, brillo, y potencia. A continuación, se describen algunos de los elementos más comunes que utilizan PWM:

### 1. **Motores de corriente continua (DC)**
Los motores DC son dispositivos que convierten la energía eléctrica en movimiento. El uso de PWM permite controlar la velocidad del motor ajustando el ciclo de trabajo de la señal PWM. Un ciclo de trabajo alto resultará en una mayor velocidad del motor, mientras que un ciclo bajo reducirá la velocidad.

### 2. **Servomotores**
Los servomotores, utilizados en robótica y mecanismos de precisión, también usan señales PWM para controlar su posición. En este caso, la duración del pulso determina el ángulo en el que el servomotor se posicionará.

### 3. **LEDs (diodos emisores de luz)**
El brillo de un LED puede controlarse con señales PWM. Al variar el ciclo de trabajo de la señal, podemos hacer que el LED sea más brillante (con un ciclo alto) o menos brillante (con un ciclo bajo), sin cambiar su color ni comprometer la eficiencia.

### 4. **Controladores de potencia para calentadores**
Los calentadores eléctricos pueden ser controlados mediante PWM para regular la cantidad de calor que generan. Al variar el ciclo de trabajo, podemos aumentar o disminuir la potencia del calentador.

### 5. **Altavoces y generadores de tonos**
En los altavoces, el PWM puede ser utilizado para generar señales de audio de diferentes frecuencias, creando diferentes tonos musicales o sonidos.

### 6. **Fuentes de alimentación conmutadas**
Las fuentes de alimentación conmutadas utilizan PWM para regular el voltaje de salida. Al ajustar el ciclo de trabajo de la señal PWM, se puede controlar el voltaje y la corriente entregados a una carga.

## Código de ejemplo: Control de la velocidad de un motor DC con PWM

En este ejemplo, se controlará la velocidad de un motor de corriente continua (DC) utilizando una señal PWM generada por Arduino. El ciclo de trabajo de la señal se ajusta con un potenciómetro conectado a un pin analógico de Arduino.

```cpp
int motorPin = 9;  // Pin PWM conectado al motor
int potPin = A0;   // Pin analógico conectado al potenciómetro
int potValue = 0;  // Variable para almacenar el valor leído del potenciómetro
int pwmValue = 0;  // Variable para almacenar el valor PWM calculado

void setup() {
  pinMode(motorPin, OUTPUT);  // Configuramos el pin del motor como salida
}

void loop() {
  // Leemos el valor del potenciómetro (0-1023)
  potValue = analogRead(potPin);

  // Convertimos el valor del potenciómetro a un rango PWM (0-255)
  pwmValue = map(potValue, 0, 1023, 0, 255);

  // Enviamos la señal PWM al motor para ajustar la velocidad
  analogWrite(motorPin, pwmValue);

  // Pequeña pausa
  delay(10);
}
```

### Explicación del código:

- **`analogRead(potPin)`**: Lee el valor del potenciómetro, que varía entre 0 y 1023.
- **`map(potValue, 0, 1023, 0, 255)`**: Mapea el valor del potenciómetro al rango de 0 a 255, que es el rango utilizado por la función `analogWrite()` para generar señales PWM.
- **`analogWrite(motorPin, pwmValue)`**: Envia una señal PWM al pin del motor para controlar su velocidad en función de la posición del potenciómetro.

Este ejemplo muestra cómo controlar la velocidad de un motor DC utilizando un potenciómetro. La misma técnica puede aplicarse para controlar el brillo de un LED o la potencia en otros dispositivos compatibles con PWM.