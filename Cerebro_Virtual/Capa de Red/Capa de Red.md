# Capa de Red

La Capa de Red es la tercera capa del [[Modelo OSI]]. Es responsable del enrutamiento de paquetes a través de una o más redes. Se encarga de la entrega de paquetes desde el origen hasta el destino, lo que puede requerir que los paquetes atraviesen múltiples redes.

## Funciones de la Capa de Red

*   **Enrutamiento**: Determina la mejor ruta para que los paquetes lleguen a su destino. Utiliza algoritmos de enrutamiento para tomar decisiones de reenvío.
*   **Direccionamiento lógico**: Asigna direcciones únicas a los dispositivos de la red (por ejemplo, [[Direccionamiento IP]]). A diferencia del [[Direccionamiento MAC]], que es físico y local, el direccionamiento lógico es jerárquico y global.
*   **Conmutación de paquetes**: Divide los mensajes grandes en paquetes más pequeños para su transmisión. Los paquetes se vuelven a ensamblar en el destino.
*   **Control de congestión**: Evita que la red se sature de paquetes.

## Enrutamiento

El enrutamiento es el proceso de seleccionar una ruta para el tráfico en una red o entre redes. Los dispositivos que realizan el enrutamiento se llaman enrutadores.

Un enrutador tiene dos funciones principales:

*   **Reenvío**: La acción de mover un paquete de una entrada a una salida.
*   **Enrutamiento**: El proceso de determinar la ruta que debe seguir un paquete.

Los algoritmos de enrutamiento se pueden clasificar en:

*   **Adaptativos**: Se ajustan a los cambios en la topología y el tráfico de la red.
*   **No adaptativos**: Las rutas se calculan de antemano y no cambian.

## Servicios de la Capa de Red

La Capa de Red puede proporcionar dos tipos de servicios a la [[Capa de Transporte]]:

*   **Servicio orientado a la conexión (Circuitos Virtuales)**: Se establece una conexión antes de que se transmitan los datos. Esto garantiza que los paquetes lleguen en orden y proporciona un servicio fiable.
*   **Servicio no orientado a la conexión (Datagramas)**: Los paquetes se envían de forma independiente y pueden llegar desordenados. No se garantiza la entrega.
