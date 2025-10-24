# Capa de Enlace de Datos

La Capa de Enlace de Datos es la segunda capa del [[Modelo OSI]]. Su función principal es proporcionar una transferencia de datos fiable a través de un medio físico. Toma los paquetes de la [[Capa de Red]] y los encapsula en tramas para su transmisión.

## Funciones de la Capa de Enlace de Datos

*   **Entramado**: Divide el flujo de bits en unidades manejables llamadas tramas.
*   **Direccionamiento físico**: Añade una cabecera a la trama para definir el emisor y el receptor. Utiliza [[Direccionamiento MAC]].
*   **Control de flujo**: Evita que un emisor rápido sature a un receptor lento.
*   **Control de errores**: Detecta y, a veces, corrige los errores que pueden ocurrir en la [[Capa Física]].
*   **Control de acceso al medio (MAC)**: Determina qué dispositivo tiene derecho a utilizar el medio en un momento dado.

## Control de Errores

Se utilizan varias técnicas para detectar errores en los datos recibidos:

*   **Paridad**: Se añade un bit de paridad a cada byte de datos para asegurar que el número de 1s sea par o impar.
*   **Suma de comprobación (Checksum)**: Se calcula una suma de los datos y se envía junto con los datos. El receptor vuelve a calcular la suma y la compara con la suma recibida.
*   **Comprobación de redundancia cíclica (CRC)**: Un algoritmo más sofisticado que la suma de comprobación y que es muy eficaz para detectar errores.

## Control de Acceso al Medio (MAC)

Cuando varios dispositivos comparten el mismo medio de transmisión, es necesario un protocolo de control de acceso al medio para evitar colisiones. Algunos protocolos de MAC son:

*   **[[ALOHA]]**: Un protocolo simple en el que los dispositivos transmiten cuando tienen datos para enviar. Si se produce una colisión, esperan un tiempo aleatorio antes de volver a transmitir.
*   **[[CSMA (Carrier Sense Multiple Access)]]**: Los dispositivos escuchan el medio antes de transmitir. Si el medio está ocupado, esperan. Existen varias versiones de CSMA:
    *   **CSMA/CD (Collision Detection)**: Los dispositivos pueden detectar colisiones y dejar de transmitir inmediatamente.
    *   **CSMA/CA (Collision Avoidance)**: Los dispositivos intentan evitar las colisiones transmitiendo una pequeña señal de aviso antes de transmitir los datos.
