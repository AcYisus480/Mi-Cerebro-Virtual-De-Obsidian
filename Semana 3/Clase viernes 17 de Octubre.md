___

# Capa de transporte

La capa de transporte en el modelo OSI se encarga de asegurar la entrega confiable de datos entre dispositivos, controlando el flujo, la segmentación y la corrección de errores.

En general, la capa de enlace de datos y la capa de transporte, comparten tareas semejantes:
* Control de errores.
* Secuenciación.
* Control deflujo (como en enlace de datos). 

Sin embargo, hay ciertas diferencias

El objetivo de la capa de transporte es ofrecer un servicio confiable sobre una red poco confiable. Al igual que en la capa de red, se establecen dos tipos de servicio:
* Orientado a conexión.
* No orientado a conexión.

Dado que, la capa de transporte brinda servicios a las aplicaciones, es necesario ofrecer la multiplexión de los flujos de datos: ***direccionamiento de puertos.*** 

*Del servicio orientado a conexión, se desprende:*
* Establecimiento de una conexión.
* Liberación de la conexión.

El servicio orientado a conexión requiere de tres fases:
* Establecimiento de la conexión.
	* Se realiza en tres fases:
    
	    1. El nodo A envía una solicitud de conexión al nodo B.
	    2. El nodo B responde confirmando la solicitud.
	    3. El nodo A confirma la respuesta de B.
	 Una vez completado este proceso, se puede comenzar a enviar paquetes.
	
	###### Establecer una conexión puede resultar en una tarea muy complicada, debido a:

	* Cuando hay ***perdida de paquetes***, se pierde una conexión, se requiere que el nodo "a" mande la solicitud, si no se recibe una conexión en un cierto tiempo, pues lo vuelve a mandar, para esto se requiere de un ***temporizador***.
	* En otro caso, cuando hay una transmisión bastante lenta, puede mandar un segundo paquete, entonces hay ***paquetes duplicados***
	* Cuando la respuesta se pierde, el nodo a vuelve a mandar un paquete, al recibirlo "b", hay un ***paquete duplicado***.

* Transferencia de datos.
	* Ventana deslizante, es mandar bloques de paquetes en ráfaga, en donde el nodo receptor responde de igual manera por paquete. Cuando se confirma la llegada de todos los paquetes y se confirmen estos, la ventana se desliza a los siguientes n datos.
* Liberación de la conexión. 

Lo anterior no es una tarea sencilla a diferencia de un servicio no orientado a conexión, la cual solo involucra la transferencia de datos.


***La desconexión***, tampoco resulta ser un problema fácil, esta puede ser:
* Asimétrica, que puede resultar en pérdida de datos ya que se necesita que ambos nodos esten de acuerdo a la desconexión.
* Simétrica, que es útil cuando se conoce la cantidad de datos que se va a enviar, no requiere confirmación de desconexión, los datos llegarán.

En general no hay un protocolo adecuado, pero existen buenas implementaciones, por ejemplo:
* Acuerdo de tres vías (Three Way Handshake), con o sin tiempo de expiración.
* Simplemente liberar la conexión si ha pasado determinada cantidad de tiempo, sin que lleguen datos.

# Capa de sesión
En esta capa se establecen las actividades de control de dialogo y sincronización, pero a nivel aplicación. 
Las funciones principales de la capa de sesión son:
* Control de dialogo: define el turno de la transmisión.
* Administración de turno: para hacer que dos partes no realicen alguna operación al mismo tiempo. 
* Recuperación: establecer puntos de referencia en la transmisión.

# Capa de presentación 
El principal objetivo de esta capa es la de mantener las sintaxis y la semántica de los datos transmitidos. 
La capa de presentación asegura que un registro sea recibido en el otro extremo, manteniendo el orden y el mismo tipo de datos con el que salió.
Por ejemplo, cuando se manejan datos de más de un byte, ¿cuál será el formato adecuado? Conocido como: endianness.
* Big-endian, del MSB al LSB. 
* Little-endian, del LSB al MSB.
* Middle-endian.

La tarea de la capa de presentación es: 
* Cifrado de los datos.
* Compresióndelos datos.
* Formateodedatos

# Capa de Aplicación 
Es el punto de entrada para que las aplicaciones puedan transmitir información hacia un punto determinado. 
En esta capa se localizan los protocolos particulares de las aplicaciones que son empleados por los usuarios: transferencia de archivos, correo electrónico, conexión remota, entre otros.