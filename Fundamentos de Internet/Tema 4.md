## Tema 4: La capa de transporte
### Modelo simplificado de transferencia TCP

- El temporizador(timeout) en TCP, no tiene por que ser fijo, sino que puede ajustarse al tiempo de transferencia de cada paquete
- Cada ronda hace una estimación del error, además tiene en cuenta el error de la ronda anterior. 
![[temporizador_tcp.png]]
#### Otra modificación del modelo simplificado
Retransmitimos el segmento mas antiguo pero cambiamos el timeout, multiplicamos por dos el que teníamos.
>Importante: Es recomendable dibujar con precisión los tiempos en el esquema
![[doble_timeout.png]]
#### Diagrama de intercambio de mensaje
![[intercambio_de_mensajes.png]]

## Ejercicios Tema 4
![[ejc_TCP.png]]
- [ ] A No mandaría de nuevo el SN 1000 porque al haberle llegado el 3º, le ha llegado el 1º y el 2º
- [ ] B
- [ ] C No esperaría al timeout, mandaría el SN 1000 al recibir el 3º ACK
- [ ] D
- [x] E ✅ 2023-11-02
- [ ] F Manda mal los paquetes, debería haber mandado SN 2520 en el 3º y los ACK también están mal.

#### Campo ventana en TCP
El algoritmo de control de flujo de TCP se encarga de que el buffer no se llene nunca, dando un tamaño de ventana u otro. El de congestión hace algo parecido, y TCP cogerá el tamaño de ventana mas pequeño de los dos. El de flujo se encarga de ver el espacio libre en el buffer de recepción. El campo window se revisa cada vez que se recibe algo.
![[control_flujo_tcp.png]]
