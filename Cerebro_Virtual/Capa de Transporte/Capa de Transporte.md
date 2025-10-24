# Capa de Transporte

La Capa de Transporte es la cuarta capa del [[Modelo OSI]]. Su función principal es proporcionar una comunicación de extremo a extremo fiable y transparente entre las aplicaciones. Toma los datos de la [[Capa de Sesión]] y los divide en segmentos para su transmisión.

## Funciones de la Capa de Transporte

*   **Segmentación y reensamblaje**: Divide los datos en segmentos en el origen y los vuelve a ensamblar en el destino.
*   **Direccionamiento de puertos**: Permite que varias aplicaciones en un mismo host se comuniquen simultáneamente. Cada aplicación tiene un número de puerto único.
*   **Control de conexión**: Establece, mantiene y termina las conexiones entre las aplicaciones.
*   **Control de flujo**: Evita que un emisor rápido sature a un receptor lento.
*   **Control de errores**: Garantiza que los datos lleguen sin errores, en orden y sin duplicados.

## Servicios de la Capa de Transporte

La Capa de Transporte ofrece dos tipos de servicios a las capas superiores:

*   **Servicio orientado a la conexión**: Proporciona una comunicación fiable. Se establece una conexión antes de que se transmitan los datos, y se garantiza que los datos lleguen en orden y sin errores. El protocolo [[TCP (Transmission Control Protocol)]] es un ejemplo de servicio orientado a la conexión.
*   **Servicio no orientado a la conexión**: Proporciona una comunicación no fiable. Los datos se envían sin establecer una conexión, y no se garantiza que lleguen en orden o sin errores. El protocolo [[UDP (User Datagram Protocol)]] es un ejemplo de servicio no orientado a la conexión.

## Establecimiento y Liberación de la Conexión

El establecimiento de una conexión en un servicio orientado a la conexión suele implicar un proceso de tres vías (Three-Way Handshake):

1.  El cliente envía una solicitud de conexión (SYN).
2.  El servidor responde con una confirmación (SYN-ACK).
3.  El cliente confirma la respuesta (ACK).

La liberación de la conexión también puede ser un proceso de varias vías para garantizar que no se pierdan datos.
