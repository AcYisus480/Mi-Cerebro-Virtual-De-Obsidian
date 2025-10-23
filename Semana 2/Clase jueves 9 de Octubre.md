___
### Modelo de tres capas

***Dificultades a resolver:***

1. "Entrada" o servicios para las diversas aplicaciones o usuarios al mismo tiempo.
2. Asegurar que los datos lleguen a su destino y en orden.
3. Una interfaz con hardware que se encargará de "colocar" los datos en el medio de comunicación.
*En este modelo haremos tres capas donde cada una de las capas resuelva cada uno de los tres problemas.*
##### Capas: 
* Aplicación: La cual contiene la lógica necesaria para soportar varias aplicaciones de usuario.
* Transporte: en donde los datos que provienen de la capa de aplicación se empaquetan y se asegura que los datos lleguen en determinado orden y seguro.
- Acceso a la red: encargada de asegurarse de que los datos lleguen a la dirección destino por medio de la red.

> [!NOTE] Notas
> * Fragmentar la información es lo que se conoce como ***empaquetamiento***.
>   *Payload es el fragemento de información segmentado.*
> * El ***encabezado*** es la redundancia que se le agrega a los paquetes, también contienen número de secuencia en la que se conoce el orden en que se tiene que ordenarse.

Cuando un paquete ya esta empaquetado, y es recibida por el paquete de acceso a la red necesita empaquetar de nuevo el paquete, agregándole de nuevo el encabezado, ya que el receptor necesita validar que todo esta en orden.

el que se agregue información a los paquetes, es necesario, ya que se determina por el **protocolo**

#### En general:
La información que se trasmite, no se transmite de manera constante o es muy complicado, se transmite por ráfagas.
Lo que se hace es fragmentar esa información que se va a transmitir en pequeñas unidades.
Esas unidades se llaman: (PDU) Unidades de datos de protocolo.

Una condición para que dos aplicaciones puedan comunicarse entre si es que pertenezcan a la misma red, cuando tenemos aplicaciones en diferentes redes, tenemos otros problemas, ya que posiblemente no contamos con el mismo protocolo de comunicación.
Entonces:
###### Otros aspectos a considerar:
- Direccionamiento/enrutamiento.
- Sintaxis, formato de los datos.
- Semántica, información de control.
- Temporización, sincronización de velocidad y secuenciación.
- Control de errores.
- Control de flujo
- Multiplexación.

#### Tipo de servicio

Un concepto muy importante en el modelo a capas es el tipo de servicio, el cual se refiere a la manera de mantener el enlace en la comunicación.

Las capas pueden ofrecer dos tipos de servicio:

- Orientado a conexión.
	- Secuencia.
	- Flujo.
- No orientado a conexión
	- Con confirmación.
	- Sin confirmación.
##### Protocolos y Servicios
1. Los servicios son las primitivas u operaciones. No es necesario saber como se hacen las operaciones. Los servicios son entre capas.
2. El protocolo son las reglas de comunicación entre las *capas pares*.

Existen varios modelos de referencia de redes, nos enfocaremos en estos dos:
* Modelo OSI
* Modelo TCP/IP

Los principios del modelo ***OSI*** son:
- Cada capa debe tener una función especifica.
- La intención de cada capa es definir protocolos estandarizados.
- Minimizar el flujo de información entre capas.
- Número óptimo de capas.

Las capas del modelo ***OSI*** son:
- Aplicación: proporcionada el acceso a los usuarios.
- Presentación: servicios en la representación de los datos.
- Sesión: control de la comunicación entre las aplicaciones.
- Transporte: proporciona una transferencia transparente y fiable de los datos.
- Red: proporciona técnicas de conmutación y de transmisión para conectar a los sistemas.
- Enlace de datos: transferencia de datos a través de un enlace físico.
- Física: transmisión de los datos sobre el medio físico.

![[Imagen de WhatsApp 2025-10-07 a las 13.12.16_67dbd95a.jpg|400]]


