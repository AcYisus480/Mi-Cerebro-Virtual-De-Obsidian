# Capas Superiores

Las capas superiores del [[Modelo OSI]] (Sesión, Presentación y Aplicación) se encargan de las funciones de comunicación más cercanas al usuario.

## Capa de Sesión

La Capa de Sesión es la quinta capa del [[Modelo OSI]]. Es responsable de establecer, gestionar y terminar las sesiones de comunicación entre aplicaciones. Una sesión es un diálogo semipermanente entre dos o más dispositivos.

### Funciones de la Capa de Sesión

*   **Control de diálogo**: Decide qué dispositivo transmite, cuándo y por cuánto tiempo.
*   **Agrupación**: Agrupa los datos en unidades lógicas.
*   **Recuperación**: Si se produce un fallo, la capa de sesión puede reanudar la comunicación desde un punto de control anterior.

## Capa de Presentación

La Capa de Presentación es la sexta capa del [[Modelo OSI]]. Se encarga de la sintaxis y la semántica de la información transmitida. Garantiza que los datos enviados por la capa de aplicación de un sistema puedan ser leídos por la capa de aplicación de otro sistema.

### Funciones de la Capa de Presentación

*   **Traducción**: Convierte los datos a un formato común antes de la transmisión.
*   **Cifrado**: Cifra los datos para garantizar la confidencialidad.
*   **Compresión**: Comprime los datos para reducir el número de bits que hay que transmitir.

## Capa de Aplicación

La Capa de Aplicación es la séptima y más alta capa del [[Modelo OSI]]. Es la capa que está más cerca del usuario y proporciona servicios de red a las aplicaciones del usuario. Es la única capa que no proporciona servicios a ninguna otra capa OSI.

### Funciones de la Capa de Aplicación

*   **Identificación de los interlocutores**: Determina si el interlocutor deseado está disponible.
*   **Sincronización**: Sincroniza la comunicación entre las aplicaciones.
*   **Protocolos de aplicación**: Proporciona los protocolos que utilizan las aplicaciones, como:
    *   **[[HTTP (Hypertext Transfer Protocol)]]**: Para la navegación web.
    *   **[[FTP (File Transfer Protocol)]]**: Para la transferencia de archivos.
    *   **[[SMTP (Simple Mail Transfer Protocol)]]**: Para el correo electrónico.
    *   **[[DNS (Domain Name System)]]**: Para la resolución de nombres de dominio.
