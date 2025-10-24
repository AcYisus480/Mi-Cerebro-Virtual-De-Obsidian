# Arquitectura de Redes
## Clase 1. Introducción.

---

# Introducción a las Redes
Fuente -> Transmisor -> Medio de transmisión -> Receptor -> Destino

**Representación (señales):**
*   Señal (digital/analógica).
*   Amplitud, fase, frecuencia y ancho de banda.
*   Velocidad de transmisión vs ancho de banda.
*   Atenuación, distorsión (atenuación y retardo), ruido.
*   Medio de transmisión: guiado y no guiado. Simplex, half-duplex y full-duplex. En el caso digital, también podemos hablar de: paralelo y serial.

---

# Transmisión
La transmisión de señales, independientemente de su naturaleza, puede ser digital o analógica.

| Señal Analógica | Señal Digital |
| --- | --- |
| **Señal Analógica** | |
| * La señal ocupa el mismo espectro. | Digitalización. |
| * La señal o datos analógicos se codifican. | |
| **Señal Digital** | |
| Se emplea modem para general señales analógicas. | * Se hace de niveles de voltaje. |
| | * Los datos se codifican para generar una señal digital con las propiedades adecuadas. |

---

# Transmisión
**Ejemplos:**
**Analógica – Analógica (modulación)**
*   Modulación en amplitud (AM).
*   Modulación en frecuencia (FM).

---

# Transmisión
**Ejemplos:**
**Digital – Analógica (modulación)**
*   Modulación por desplazamiento de amplitud (ASK - Amplitude Shift Keying).
*   Modulación por desplazamiento en frecuencia (FSK - Frequency Shift Keying).
*   Modulación por desplazamiento en fase (PSK - Phase Shift Keying).
*   Quadrature PSK.

---

# Transmisión
**Ejemplos:**
**Digital – Digital (codificación)**
*   No retorno a cero (NRZ - Non Return to Zero)
*   No retorno a cero invertido (NRZI)
*   Bipolar AMI
*   Manchester
*   Manchester diferencial

---

# Introducción a las Redes
Fuente -> Transmisor -> Medio de transmisión -> Receptor -> Destino

Sin embargo, en el modelo intervienen una serie de elementos o inconvenientes, entre los que destacamos:
*   Interfaces.
*   Representación.
*   Sincronización.
*   Gestión de intercambio.
*   Detección y corrección de errores.

---

# Introducción a las Redes
*   Interconexión de más de dos elementos: red (network). Una red consiste de un cierto número de dispositivos autónomos (digitales) interconectados.
*   Presentación/Formato del mensaje.
*   Seguridad.
*   Direccionamiento/Encaminamiento.
*   Control de flujo.
*   Recuperación.
*   Cambios en la estructura o topología de la red.

---

# Introducción a las Redes
La red puede tener diversos tamaños, y lo conocemos como tipos de redes:
*   Local Area Network (LAN).
*   Wide Area Network (WAN).
*   Metropolitan Area Network (MAN).
*   Personal Area Network (PAN).
*   Home Area Network (HAN).

La principal razón de una red es compartir hardware y software.

---

# Introducción a las Redes
Hasta este punto, todo lo anterior se percibe altamente relacionado con hardware, sin embargo, el software juega un papel importante, ya que es que se encarga de los servicios que se ofrecerán para que los datos lleguen de un origen a un destino.

Dada la gran cantidad de problemas y elementos, la idea es implementar un conjunto de capas o módulos, que ofrezcan servicios, ocultando su funcionamiento interno.

---

# Arquitectura de red
Debido a la complejidad del sistema de comunicación, esta actividad se divide en tareas, y cada una de ellas se realiza por separado.
*   Cada tarea es realizada por un determinado módulo y cada uno de ellos, realiza una tarea de manera independiente.
*   Los distintos módulos se acomodan formando una pila vertical.
*   De esta manera cada capa proporciona un conjunto de servicios a la capa anterior.

---

# Arquitectura de red
*   Desde luego, como la comunicación se realiza entre dos entidades, en el otro lado debe existir el mismo conjunto de funciones.
*   Las capas correspondientes con las que intercambia información; esto se conoce como capas pares.
*   El intercambio de información que realizan las capas pares se hace siguiendo determinadas reglas, denominadas protocolos.
*   Entre cada capa, existe lo que se conoce como interfaz.

---

# Arquitectura de red
Una arquitectura simplificada sería:
Aplicación <-> Aplicación
Servicio de comunicaciones <-> Servicio de comunicaciones
Acceso a la red <-> Red <-> Acceso a la red

---

# Arquitectura de red
Una estructura que consiste en un grupo de módulos, que realizarán en conjunto la función de comunicación y sus protocolos, se le conoce como arquitectura de red.

La lista de protocolos que hay en cada capa, se le conoce como pila de protocolos.

---

# Arquitectura de red
**Modelo a capas**
Interfaz capa superior, la cual pide un servicio
<->
CAPA n <--> Protocolo, capas pares
<->
Interfaz capa inferior, la cual hace un servicio.

---

# Arquitectura de red
**Ejemplo: modelo de tres capas.**
Dificultades a resolver:
a) “Entrada” o servicios para las diversas aplicaciones o usuarios.
b) Asegurar que los datos lleguen a su destino y en orden.
c) Una interfaz con hardware que se encargará de “colocar” los datos en el medio de comunicación.

---

# Arquitectura de red
**Ejemplo: modelo de tres capas:**
En este pequeño modelo, solo se consideran tres capas, las cuales son:
*   Aplicación: la cual contiene la lógica necesaria para soportar varias aplicaciones de usuario.
*   Transporte: en donde los datos que provienen de la capa de aplicación se empaquetan y se asegura que los datos lleguen en determinado orden y seguros.

---

# Arquitectura de red
*   Acceso a la red, en cargada de asegurarse de que los datos lleguen a la dirección destino por medio de la red.

SAPs (Service Access Point) o puertos
Aplicación (1)(2)(3)
Transporte
Acceso a la red

La información fluye entre capa y capa, en unidades de datos de protocolo (PDU, Protocol Data Unit).

---

# Arquitectura de protocolos
**Modelo de tres capas:**
Aplicación <---Protocolo de aplicación---> Aplicación
Transporte <---Protocolo de transporte---> Transporte
Acceso a la red <---Protocolo de acceso a la red---> Red <---Protocolo de acceso a la red---> Acceso a la red

---

# Arquitectura de red
**Modelo de tres capas:**
Aplicación <---Datos---> Aplicación
Transporte <---CT | Datos---> Transporte
Acceso a la red <---CR | CT | Datos---> Acceso a la red

---

# Arquitectura de red
**Otros aspectos a considerar:**
*   Direccionamiento/enrutamiento.
*   Sintaxis, formato de los datos.
*   Semántica, información de control.
*   Temporización, sincronización de velocidad y secuenciación.
*   Control de errores.
*   Control de flujo.
*   Multiplexación.

---

# Arquitectura de red
Un concepto muy importante en el modelo a capas es el tipo de servicio, el cual se refiere a la manera de mantener el enlace en la comunicación.

Las capas pueden ofrecer dos tipos de servicio:
*   Orientado a conexión.
    *   Secuencia.
    *   Flujo.
*   No orientado a conexión.
    *   Con confirmación.
    *   Sin confirmación.

---

# Arquitectura de red
**Muy importante entre Protocolos y servicios:**
1.  Los servicios son las primitivas u operaciones. No es necesario saber cómo se hacen las operaciones. Los servicios son entre capas.
2.  El protocolo son las reglas de comunicación entre las capas pares.

---

# Fin de la clase 1
