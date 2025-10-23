___
# Modelo OSI

## Capa Física: medio de transmisión
De manera general, la capa física se encarga de transportar los datos de un punto a otro; y para ello tiene que hacer uso de algún medio o canal. Los medios de transmisión se clasifican en:

- Medio guiados.
  Cuando las señales se propaga por todo el medio fisico, como cables
- Medios no guiados.
  Cuando se propagan por medio no fisico, como el aire.

Medios Guiados: 
* Par trenzado, este es el medio mas común y consistente de un par de alambres de cobre trenzados entre si de esta manera se disminuye la interferencia.
- El par trenzado se puede emplear tanto en comunicaciones analogicas y digitales.
- el ancho de banda depende del grosor del cable y la distancia que recorre.
- existen varios tipos de par trenzado a cada tipo dse le conoce como categoria: 3, 4 , 5, 6, 7.
* Las categorias 6 y 7 tienen anchos de banda de 250 MHz y 600 MHz
- Las categorias 3 y 5 tienen anchos de banda de 16MHz y 100 MHz
- A este cable tambien se le conoce como UTP

![[Pasted image 20251010122805.png|400]]

*Las normas tienen que ser la misma en ambos extremos*
Hay cables directos y cables cruzados.

#### Medios guiados: cable coaxial 
- El cable coaxial consiste de un alambre de cobre rodeado de aislante y de un conductor cilíndrico. 
- Tiene un mejor blindaje que el par trenzado, por lo que puede abarcar tramos más grandes a velocidades mayores.
- Existen dos tipos de cables: el de 50 ohm para comunicaciones digitales, y el de 75 ohm para comunicaciones analógicas.

![[Pasted image 20251010123019.png|400]]


Enlaces unicos o simple, se lleva a cabo en la red, es donde un dispositivos se quiere conectar con otro y esto se hace por medio de un par trensado,donde ningun otro nodo o dispositivo tiene acceso a la concexión, el encargado de hacer esto es el conmutador.

Enlace compartido. es cuando dos nodos se conectan y los demas nodos tienen acceso a la comunicación (pueden ver la comunicación).

#### Medios guiados: fibra óptica
- Es una fibra delgada de algún material transparente, el cual puede ser vidrio o plástico, por el cual se hace pasa un haz de luz que lleva la información. 
- De manera general, un sistema de transmisión óptico posee tres elementos: la fuente de luz, el medio de transmisión y un detector. 
- La fuente de luz genera un pulso de luz, el cual es enviado al detector por medio de la fibra.

Fribras monomodo, donde pueden haber solo un solo haz de luz
fibras multimodo, donde pueden haber varios haz de luz

Una fibra monomodo puede tener velocidades de transmisión de más de 50Gbps, en cambio un multimodo ronda los 10Gbps.

- Existe un ángulo crítico, a partir del cual el rayo de luz se reflejaría completamente; por lo tanto, podríamos tener muchos rayos de luz a diferentes ángulos de reflexión. Esto se conoce como fibra multimodo.
- Si se hace la fibra muy delgada, se permite que el haz se pueda propagar casí en línea recta; esto se conoce como fibra monomodo.

##### Medios no guiados: espectro electromagnético
- Es la distribución de energía de un rango de ondas electromagnéticas.
- La distribución se realiza considerando la frecuencia de cada onda, la cual puede ir desde unos cuantos Hertz hasta varios millones de Hertz.
- No todo el espectro de frecuencias es útil, solo se emplea un determinado rango de él.

![[Pasted image 20251010125023.png|400]]


##### Capa Física 
En términos generales, la Capa Física, está destinada a trabajar con la transmisión de los bits sobre un canal de comunicación, estos bits son convertidos a señales eléctricas por lo que deben codificarse o aplicar algún método de modulación. 
Es importante mencionar que, en esta capa no se define como tal un protocolo, en todo caso, se podría hablar de una conversión.

En general, dentro de la Capa Física se tratan con problemas tales como: 
- Tipo de señales eléctricas para representar los símbolos.
- Tiempodebit(tb).
- Simplex, Half-Duplex o Full-Duplex. 
- Aspectos físicos de los conectores (forma, número de pines, etc.).

#### Capa de Enlace de Datos
Esta capa “transforma” el medio de transmisión en una línea de comunicación libre de errores. De esta forma, proporciona un servicio de transferencia de datos seguro a través de un medio físico.

##### Capa de Enlace de Datos Se encarga de:
- Organizar los patrones o flujos de bits en bloques o paquetes denominados tramas (frames), se encarga de su sincronización.
- Manejo de errores que resulten de la trasmisión física de los bits.
- Control de flujo, es decir, controla la velocidad con la cual la fuente envía los datos, en función de la capacidad del buffer del receptor (transmisor rápido vs receptor lento).

En algunos casos, cuando el medio es compartido, como podría ser un bus o el espacio libre, dado que todos los elementos de la red emplean las mismas señales al momento de transmitir, es importante sincronizar el acceso al medio. 
En la Capa de Enlace de Datos, se encuentra una subcapa llamada Control de Acceso al Medio, encargada de controlar el acceso al canal compartido.

A partir de esta capa, ya se habla de protocolos. Las funciones de los protocolos son:
- Encapsulamiento. Agrega información de control. PDU(Protocol Data Unit), estructura del paquete. 
- Segmentación y ensamblado.
- Control de conexión. Establecimiento, transferencia y cierre.
- Entrega en orden. 
- Control de Flujo.
- Control de errores.