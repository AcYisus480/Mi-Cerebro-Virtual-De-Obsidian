___

# Modelo OSI

### Protocolos
###### Algunas de las funciones de los protocolos son:
* **Encapsulamiento.**
  Agrega información de control. PDU(Protocol Data Unit), estructura del paquete.
* **Segmentación y ensamblado.**
* **Control de conexión.** 
	* Establecimiento
	* Transferencia 
		* Errores que se encuentran aquí:
			* Retardo
			* Perdidas
	* Cierre.
* Entrega en orden.
* Control de Flujo.
* **Velocidad de entrega.**
	* Cantidad de paquetes que se entregan en un determinado tiempo (Velocidad de bits y velocidad de paquetes).
* **Control de Errores.**
	* Identificar cuando un paquete llega correctamente.
	* También puede tener corrección de errores, lo que implica redundancia.
* **Multiplexación.** 
	* El encaminado de flujos de datos que tienen que pasar por un solo camino.
		* *Ascendente.*
			* De los datos recibidos, se requiere que los datos vayan a la respectiva aplicación, por lo que requiere que se vayan por el mismo camino y al final tomen su propio camino.
		* *Descendente.*
			* De múltiples aplicaciones que se requiere transmitir a otro nodo el flujo tiene que ser por un mismo canal
* Servicio de transmisión. 
	* Prioridad.
	* Calidad de servicio.
	* Seguridad. 
* Tamaño de mensaje. 
* Tiempos de espera.

### Capa física
En general esta capa es la que se encarga de transmitir los bits de un medio a otro por medio de un canal de comunicación, la capa física no se le implementa protocolos.

### Capa de enlace de datos
Esta capa “transforma” el medio de transmisión en una línea de comunicación libre de errores. De esta forma, proporciona un servicio de transferencia de datos seguro a través de un medio físico.

###### Esta capa se encarga de:
* Organizar los patrones o flujos de bits en bloques o paquetes denominados tramas (frames), formato de datos, y se encarga de su sincronización.
* Manejo de errores que resulten de la trasmisión física de los bits.
	* Métodos de detección de errores:
	  *Solo se agrega un bit a los paquetes*
		* ***Paridad Par :***
		  La cantidad de unos tiene que ser par, el bit agregado tiene que corresponder a esto, por ejemplo, si hay una cantidad impar de bits, se agrega un uno para que sea par, en otro caso, si la cantidad de bits es par, simplemente se agrega un cero.
		* ***Paridad impar :***
		  Es lo mismo que lo anterior mencionado, simplemente que es en el caso de impar.
		* Un caso mas elaborado se puede hacer en dos dimensiones.
		  Usando una matriz de $n \;x\; m$ se le agrega una columna y una fila extra, donde se agrega un bit de acuerdo a la fila asociada o a la columna. Con esto podemos detectar especificamente el error.
* Control de flujo. Controla la velocidad con la cual la fuente envía los datos en función de la capacidad del buffer del receptor (transmisor rápido vs receptor lento)

En algunos casos, cuando el medio es compartido, como podría ser un bus o el espacio libre, dado que todos los elementos de la red emplean las mismas señales al momento de transmitir, es importante sincronizar el acceso al medio. 

En la Capa de Enlace de Datos, se encuentra una subcapa llamada Control de Acceso al Medio, encargada de controlar el acceso al canal compartido.

Cuando estamos en una red, con mas de dos nodos, al querer comunicarnos especificamente con un nodo, requerimos de ***direccionamiento***.

Cuando dos nodos transmiten al mismo tiempo, se menciona que habra un colisionamiento en el medio de transmisión, y esto implica que los paquetes van a destruirse, consecuentemente los nodos que iban a recibir la inrofmación, recibiran basura.

Para esto necesitamos con control de acceso al canal compartido, para que los nodos puedan transmitir su paquete a la vez.

Uno de los algoritmos de control de acceso al medio se llama *ALOHA*, es un algoritmo básico.

```console
Inicio
  Mientras el nodo tenga datos para enviar:
    Transmitir paquete
    Esperar confirmación (ACK) durante un tiempo límite

    Si se recibe ACK:
      El paquete fue recibido correctamente
      Preparar el siguiente paquete
    Sino:
      Colisión detectada
      Esperar un tiempo aleatorio (backoff)
      Retransmitir el paquete
  FinMientras
Fin
```

### Capa física y enlace de datos
Hasta este punto, con estas dos capas, podemos hablar de redes punto a punto o de canal de difusión. Sin embargo, ¿Qué sucede cuando los datos deben viajar o pasar a través de uno o varios nodos, o una o varias redes?, simplemente no se puede, necesitamos de una capa de transmisión de datos. Esta capa se llama ***Capa de red***.

### Capa de red
* ¿Cuántas rutas existen para llegar de un punto a otro?
* ¿Cómo determinar esas rutas?
* ¿Quién elige la ruta? ¿Con qué criterio?
* Una vez establecida la ruta, ¿está siempre permanece? 

Observe que la capa de enlace de datos solo mueve de un extremo a otro del canal o medio de transmisión; en cambio, la capa de red mueve de un punto a otro.
###### La capa de red es la encargada de: 
* Escoger las rutas para no sobrecargar las líneas de comunicación, lo que conocemos como ***congestión.*** Por lo tanto, es necesario implementar un control de la congestión.
* Transmisión de un extremo a otro.
* Direcciones de red.
###### La capa de red proporciona dos tipos de servicio:
* Orientado a conexión, en donde la calidad de servicio predomina al proporcionar un servicio confiable: circuito virtual (CV).
* No orientado a conexión, en donde la información simplemente se mueve de un punto a otro y no se realiza ninguna otra acción, típicamente conmutación de paquetes.