# Introducción al funcionamiento de las redes
## Índice

1. Introducción
2. Interconexión entre computadores en la red
	1. Conexión directa
	2. Conexión indirecta
3. Introducción a Internet
## Introducción
Hasta ahora las apps que hemos trabajado trabajaban "por su cuenta" por así decirlo, pero ahora que vamos a usar internet deberemos ver las diferencias entre estas apps "solitarias" y las apps distribuidas. 
Las aplicaciones se dice que son distribuidas cuando están distribuidas entre varios equipos, por ejemplo tenemos estas dos apps que se comunican de la siguiente forma:
``` C
#include<stdio.h>
#include<net.h>
struct msg{
	int a;
	int b;
};
int suma;
fscanf("%d, %d", &(msg.a), &(msg.b));
send(ComputerB, pid=14, msg);
receive(&suma);
```
Ese es el código de la maquina cliente, a continuación vemos el código de la máquina servidor:
```C
#include<stdio.h>
#include<net.h>
struct msg{
	int a;
	int b;
};
int suma;
receive(&msg);
suma = msg.a + msg.b;
send(ComputerA, pid = 10, suma)
```

Teniendo en cuenta que ya sabemos qué es una aplicación distribuida, vamos a ver qué es una red de ordenadores. Una red de ordenadores es un conjunto de maquinas interconectadas que intercambian información, por ejemplo un smartphone, un portátil o una smart TV se interconectan entre ellas en la red WiFi de tu casa. ¿Qué demonios es una red entonces? Pues es un sistema que concede conexión entre equipos/nodos.

## Los cuatro modos de Conexión
Básicamente existen 4 modos de interconectar nodos dentro de una red. La primera, la más intuitiva y simple es a través de un enlace punto a punto. 
### Enlace punto a punto
Dos nodos conectan sus tarjetas de red(o NIC en inglés) y transmiten información entre ellos. Los bits fluyen a través del medio físico.
#### NIC (network adapters)
Es una combinación de Hardware, Software and Firmware. Sirven para transmitir y recibir datos fuera del equipo. Cada NIC posee un nombre propio y único, tienen un formato de este estilo(este es solo un ejemplo):
```
c0:18:03:88:f2:94
```
![[NIC.png]]

#### Operaciones básicas entre NIC
Vamos a poner un ejemplo rápido y sencillo de una conexión entre dos equipos:
1. El código A llama/recibe funciones/métodos para mandar/recibir bytes a/desde un código remoto.
2. El sistema operativo A ordena a la tarjeta de red que mande los bytes(empaquetados)
3. La tarjeta de red transmite los bytes al medio físico
4. La señal recorre su camino por el cable
5. El NIC B recibe la señal, recibe el paquete y se lo dice al sistema operativo
6. El sistema operativo B guarda los bytes en un buffer y llama a la app
7. La app B lee los bytes y los usa
#### El problema de la fiabilidad
Pongamos el siguiente caso, mi NIC A manda  "101101" al NIC B, al cual le llega "101111", lo cual es erróneo, por lo que deberemos buscar una forma de solucionarlo, ¿no?. Pues como todo en telemática, lo solucionaremos a través del código
![[fiabilidad NIC.png]]

#### Solución: Encapsulación
La solución puede parecer rara, pero en realidad es muy lógica, vamos a encapsular los paquetes, es decir, a todos los paquetes les vamos a añadir un encabezado(encapsulado) y el destinatario los leerá y des encapsulará. Por ejemplo vamos a poner en el encabezado un 1 si el numero de 0 en el paquete es par, y el destinatario sabrá rápidamente si el paquete que le ha llegado es correcto o no.

> Definición: Caudal(Throughput)
> Es el número de bytes que pasa por un sistema, por ejemplo, una app que puede mandar un "Hola" a la app B cada segundo. Hay diferentes standards, entre aplicaciones es de 4 bytes/sec(32bps) y entre NIC's de 13 bytes/sec(104bps)


#### Inconvenientes del enlace punto a punto
1. Hay una distancia máxima entre los nodos
2. Es muy costoso si hay mas de 2 nodos en la red(aunque hay diferentes formas de interconectarlos)
![[Nodos.png]]
### Enlace de puente or shared (broadcast) data link
Aqui conectamos multiples