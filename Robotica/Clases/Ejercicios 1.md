## Ejemplo encender led con pulsador

```c++
#define BUTTON_PIN 4
#define led 2 

void setup() {
pinMode(BUTTON_PIN, INPUT); 
pinMode(led, OUTPUT);
}
 void loop() { 
EstadoBoton = digitalRead(BUTTON_PIN);

 if EstadoBoton == LOW) {
	digital write(led, HIGH); 
} else{
 	digital write (led, LOW);
	}

} 
```
![[Ejc1.png]]

## Ejercicio adicional

Disponemos de tres leds (rojo, amarillo y verde) con la ayuda de un pulsador cambiaremos el led que está encendido. Primero tendremos el led verde encendido, si pulsamos el botón encendemos el amarillo y apagamos el verde y si volvemos a pulsar encendemos el led rojo y apagamos los otros dos.

**Propuesta de ampliación: Automatizar el semáforo y usar el botón como aviso de que hay un peatón esperando, indicaremos con un led de peatón que puede pasar y el semáforo pasará a estar en rojo para los coches.**

### Posible solucion

![[Pasted image 20250309171736.png]]![[Pasted image 20250309171740.png]]
