___
# Modelo TCP / IP

### Capa fisica
La capa fisica comparte muchas caracteristicas con el modelo OSI

Conceptos importantes: 
* Nodo: Dispositivos conectados a la red, como computadoras, enrutadores.
* Host: Cualquier dispositivo que es capaz de generar y recibir datos para su proceso.
* Enlace: El canal que comunica dos o mas nodos adyacentes. Deltro del enlace es posible considerar conmutadores o concentradores. Los enlaces pueden ser conpartidos o de difución.
* Enlace unico: une en sus extremos a dos nodos.

### Capa de acceso a la red
Esta capa se encarga de aquellos aspectos para efectuar el enlace fisico con los nodos de la red.
En esta capa existen varios protocolos que permiten crear una especie de interfaz entre el host y el hardware.

Principalmente es enviar los datos a través de un medio de comunicación.

Esta capa esta encargada de:
* Encapsulamiento
* Acceso al enlace
* Control de errores
* Control de flujo
* Direccionamiento

***Entramado:***
Consiste en diseñar un bloque de bits que contenga los datos, de tal manera que sea sencillo para el receptor encontrar el inicio y el fin del bloque.

Algunos ejemplos para lograr esto es:
* Conteo de bytes
* Bits de bandera
* Violaciones de codificación

#### Acceso al enlace
Existen dos tipos de enlace
* punto a punto
* difusión

Cuando dos o mas nodos transmiten al mismo tiempo, se dice que colisionan, para esto se requiere protocolos de acceso múltiple , por ejemplo:
* Particionamiento del canal
* Acceso aleatorio
* Tomas de turnos

``` console
Inicializar:
  Definir SLOT_DURATION
  Definir probabilidad_de_transmision (p)
  Definir estado del nodo como "esperando"

Mientras el nodo esté activo:
  Esperar hasta el inicio del siguiente slot de tiempo

  Si el nodo tiene un paquete para enviar:
    Generar un número aleatorio r entre 0 y 1
    Si r < p:
      Transmitir el paquete en este slot
      Esperar confirmación de recepción (ACK)

      Si ACK recibido:
        Eliminar paquete de la cola
        estado ← "esperando"
      Sino:
        estado ← "retransmitir"
    Sino:
      estado ← "esperando"
  Sino:
    estado ← "esperando"

  Si estado = "retransmitir":
    Esperar hasta el siguiente slot
    Reintentar transmisión con probabilidad p  
```

***CSMA***
La idea básica, es antes de transmitir primero escuchar el canal.
Ejemplo de algunos modelos:
* ***CSMA persistente***
	* Si el canal está libre, transmite de inmediato. Si está ocupado, sigue escuchando hasta que se libere.
* ***CSMA no persistente***
	* Si el canal está ocupado, espera un tiempo aleatorio antes de volver a escuchar.
* ***CSMA p-Persistente***
	* Si el canal está libre al inicio del slot, transmite con probabilidad ***p***, o espera al siguiente slot con probabilidad ***(1-p)***.

En CSMA sueden existir colisiones, en este caso, espera un tiempo aleatorio

###### Investigar sobre CSMA/CD y CSMA/CA
¿Cómo saber si un protocolo es bueno o malo?

Se realizara un análisis y se obtienen algunas métricas como el throughput o caudal.

Control de errores:
* Errores dentro de las tramas
* Tramas en orden inapropiado
* Desaparición de tramas

Códigos detectores
* paridad
* sumas de comprobación
* CRC

