# Direccionamiento

El direccionamiento es el proceso de asignar una dirección única a cada dispositivo en una red. Esto permite que los datos se envíen al destino correcto.

## Direccionamiento Físico (MAC)

La dirección de Control de Acceso al Medio (MAC) es una dirección física única que se asigna a la tarjeta de interfaz de red (NIC) de un dispositivo. La dirección MAC se utiliza para la comunicación dentro de una red local (LAN).

Una dirección MAC consta de 6 bytes, que generalmente se escriben en formato hexadecimal (por ejemplo, `00:1A:2B:3C:4D:5E`). Los primeros 3 bytes identifican al fabricante de la NIC.

## Direccionamiento Lógico (IP)

La dirección de Protocolo de Internet (IP) es una dirección lógica que se utiliza para la comunicación a través de redes. A diferencia de la dirección MAC, que es permanente y está vinculada al hardware, la dirección IP puede cambiar.

Existen dos versiones de IP:

*   **IPv4**: Una dirección de 32 bits que se escribe como cuatro números decimales separados por puntos (por ejemplo, `192.168.1.1`).
*   **IPv6**: Una dirección de 128 bits que se escribe como ocho grupos de cuatro dígitos hexadecimales separados por dos puntos (por ejemplo, `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).

## Protocolo de Resolución de Direcciones (ARP)

El Protocolo de Resolución de Direcciones (ARP) se utiliza para encontrar la dirección MAC de un dispositivo cuando se conoce su dirección IP. Funciona de la siguiente manera:

1.  Un dispositivo envía un mensaje de difusión (broadcast) a toda la red local, preguntando "¿Quién tiene la dirección IP `x.x.x.x`?".
2.  El dispositivo con esa dirección IP responde con un mensaje que dice "Yo tengo esa dirección IP, y mi dirección MAC es `yy:yy:yy:yy:yy:yy`".
3.  El dispositivo original ahora sabe a qué dirección MAC enviar los datos.

## Tipos de Comunicación

*   **Unicast**: Comunicación de uno a uno.
*   **Multicast**: Comunicación de uno a varios.
*   **Broadcast**: Comunicación de uno a todos.
