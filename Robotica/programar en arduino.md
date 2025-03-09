## La [[Funciones|funcion]] setup y loop

En Arduino, la [[funciones ino|funcion]]  `setup()` se ejecuta una vez al iniciar el programa y es donde se configuran los pines de entrada o salida, inicializaciones de comunicación, entre otras cosas. Por ejemplo: 
```cpp
void setup() { 
	pinMode(13, OUTPUT); 
}
```

La función `loop()` se ejecuta repetidamente después de `setup()`. Aquí es donde se coloca el código que queremos que Arduino ejecute en un bucle continuo:

```cpp
void loop() {
  digitalWrite(13, HIGH);
  delay(1000);
  digitalWrite(13, LOW);
  delay(1000);
}
```
## [[Tipos de datos|Variables]]
Al igual que en otros lenguajes de programación, las variables en Arduino nos permiten almacenar datos que pueden cambiar durante la ejecución del programa. Los tipos más comunes incluyen `int`, `float`, `boolean`, y `char`.
## Funciones especificas de arduino
Arduino tiene una serie de funciones integradas que permiten interactuar con el hardware. Algunas de las más comunes incluyen:

- `pinMode(pin, mode)`: Configura el pin especificado como entrada o salida.
- `digitalWrite(pin, value)`: Establece el pin en alto (`HIGH`) o bajo (`LOW`).
- `digitalRead(pin)`: Lee el estado de un pin de entrada digital.
- `analogWrite(pin, value)`: Envía una señal [[PWM]] a un pin.
- `analogRead(pin)`: Lee el valor analógico de un pin.
## Sensores y sus tipos
Los sensores se clasifican principalmente en dos tipos:

- **Sensores que reciben datos**: Como los sensores de temperatura, de luz (LDR), de distancia (ultrasonidos), etc.
- **Sensores que envían datos**: Como los actuadores, que pueden controlar motores o emitir señales luminosas o acústicas.
## Sensores que reciben datos
Estos sensores permiten que Arduino recoja información del entorno. Algunos ejemplos son:

- **Sensor de temperatura (DHT11)**: Mide la temperatura y la humedad.
- **Sensor ultrasónico (HC-SR04)**: Mide la distancia utilizando ondas de sonido.
- **LDR**: Mide la intensidad de la luz.
## Como hacemos cosas con arduino
Podemos controlar diferentes componentes electrónicos mediante Arduino, tales como:

- **Encender LEDs**: Usando `digitalWrite()`.
- **Controlar motores**: Usando un controlador de motores y la función `analogWrite()` para la velocidad.
- **Leer sensores**: Con `analogRead()` o `digitalRead()` para obtener valores de los sensores.
## Componentes basicos a la hora de hacer un proyecto en arduino

Para realizar un proyecto con Arduino, se suelen utilizar los siguientes componentes básicos:

- **Resistencias**: Controlan el flujo de corriente.
- **LEDs**: Emiten luz.
- **Motores**: Se utilizan para crear movimiento.
- **Pulsadores**: Permiten la interacción del usuario con el sistema.
- **Protoboard y cables**: Para realizar conexiones temporales.