# DIRECCIONAMIENTO DE APLICACIONES INTRODUCCIÓN A LOS SOCKETS

## Requerimientos
- Pc con Linux o Windows
- Python 3 o superior instalado
- Conocimiento minimo de Linux y Python(netscan, grep, ...)

Empezamos abriendo la terminal interactiva de Python:
![Imagen del terminal abriendo python](python_shell.png)
A continuación importamos el módulo de Socket, podemos hacerlo de varias maneras como se muestra a continuación:
```python
import socket as s
socket_udp = s.socket(s.AF_INET, s.SOCK_DGRAM)
```
O bien podemos hacerlo de la siguiente forma, la mas tradicional:
```python
import socket 
socket_tcp = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
```

Los sockets son puntos de comunicación que utilizan los procesos para intercambiar
datos entre sí. A través de ellos se pueden enviar/recibir mensajes a/desde otros
procesos que estén ejecutándose en otra una máquina remota (o local) de una forma
parecida a leer o escribir bytes en un fichero local. Nuestras aplicaciones necesitan
crear y usar sockets para “enchufarse” a la red. La siguiente figura (comentada en el
vídeo) lo ilustra.
![](esquema_sockets.png)
Existen básicamente dos tipos de sockets (en realidad hay más tipos):
- Stream sockets (de tipo flujo de bytes). Ofrecen un servicio de transporte de
	mensajes orientado a conexión y fiable. Usan el protocolo de transporte TCP.
- Datagram sockets (de tipo datagrama o carta). Ofrecen un servicio best-
	effort sin conexión previa y con mensajes de un tamaño máximo de
	65.500 bytes. Usan el protocolo de transporte UDP.

También usaremos netstat, una herramienta que nos permitirá ver los sockets en uso y filtrarlos por protocolo, puerto de salida, entrada... etc.
![](netscan.png)

Pongamos un último ejemplo antes de irnos. Vamos a abrir un server UDP, y un cliente UDP, a continuación mandaremos un mensaje desde el cliente al servidor:
Creamos el server y lo ponemos a recibir el mensaje:
![](socket_pre.png)
Creamos el cliente:
![](client_sock.png)
Y recibimos el mensaje:
![](socket_post.png)
