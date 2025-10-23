___
#### Direccionamiento
Para diferenciar a los nodos, existe un identificador único instalado en el adaptador que permite diferenciar a los nodos.
A este se le conoce como ***dirección MAC, LAN o dirección física***.
Es para diferenciar dentro de la red local y funciona para identificar a los nodos.

Se componen por 6 bytes en hexadecimal.
$$ XX:XX:XX:XX:XX:XX
$$

Los primeros tres bytes identifican al fabricante.

Tipos de comunicaciones que hay:
* ***Unicast***, comunicación de uno a uno. Un emisor envía datos a un único receptor.
* ***Multicast***, comunicación de uno a varios. El emisor transmite a un grupo específico de receptores.
* ***Broadcast***, comunicación de uno a todos. El emisor envía datos a todos los dispositivos de la red.

Cuando una computadora (o cualquier dispositivo en una red) quiere enviar datos a otra, necesita saber **cómo llegar físicamente a ella**. Es como tener el nombre de alguien pero no su dirección postal: no puedes enviarle una carta si no sabes dónde vive.

**¿Qué es ARP?**

ARP (Address Resolution Protocol) es como una guía telefónica automática. Si tienes la dirección IP del destinatario (su “nombre”), ARP te ayuda a encontrar su dirección física (MAC), que es lo que realmente se usa para enviar los datos dentro de la red local.

**¿Cómo funciona sin tecnicismos?**

1. El dispositivo dice: “Quiero hablar con la IP 192.168.1.5… ¿alguien sabe dónde está?”
2. Todos los dispositivos escuchan, y si alguno tiene esa IP, responde: “¡Esa IP soy yo! Mi dirección física es XX:XX:XX:XX:XX:XX.”
3. Ahora el primer dispositivo sabe a quién enviar los datos directamente.
___
### Capa física 

