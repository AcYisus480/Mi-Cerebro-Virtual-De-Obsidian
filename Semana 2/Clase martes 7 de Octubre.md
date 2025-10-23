
#### Transmisión
La transmisión  de señales puede ser *analógica* o *digital*.

|                 | Señal analógica                                                           | Señal digital                   |
| --------------- | ------------------------------------------------------------------------- | ------------------------------- |
| Señal analógica | ***Modulación***<br>- Ocupan el mismo espectro<br>- La señal se codifican | ***Digitalización***            |
| Señal digital   | ***Modulaci´ón***<br>*Falta mas info*                                     | - Se hace de niveles de voltaje |

##### Digital a analógica
Transformación de una señal *digital* a una *analógica* se llama ***modulación***.
###### Algunos ejemplos:
* Modulación por desplazamiento de amplitud
* Modulación por desplazamiento de frecuencia
* Modulación por desplazamiento de fase
* Quadrature PSK

###### Ejemplo de Modulación por desplazamiento de amplitud
![[Pasted image 20251007123753.png|400]]

###### Ejemplo de Modulación por desplazamiento de frecuencia
![[Pasted image 20251007123959.png|400]]

###### Ejemplo de Modulación por desplazamiento de fase
![[Pasted image 20251007124709.png|400]]

> [!NOTE] Nota
> Cambiar algunas de las propiedades de una señal se conoce como modulación

___
##### Digital a Digital
Ahora, para transformar una seña *digital* a *digital* se le llama ***Codificación***

###### Algunos métodos de transformación
* No retorno a cero
* No retorno a cero invertido
* Bipolar AMI
* Manchester
* Manchester diferencial

###### Ejemplo de digitalización por Manchester
![[Pasted image 20251007130123.png|400]]

> [!Note] Nota
> *La codificación Manchester se utiliza principalmente para sincronizar el reloj del receptor con el flujo de datos, ya que incorpora información temporal directamente en la señal.*

___

###### En el modelo de transmisión de datos existen algunos inconvenientes, entre ellos:

* **Interfaces**: Diferencias físicas o lógicas entre dispositivos que pueden dificultar la conexión o el entendimiento mutuo.
* **Representaciones**: Formatos distintos de codificar los datos (binario, ASCII, etc.) que pueden generar incompatibilidades entre sistemas.
* **Sincronización**: Necesidad de coordinar el tiempo entre emisor y receptor para interpretar correctamente los bits transmitidos.
* **Gestión de intercambio**: Control del flujo de datos para evitar pérdidas, saturación o colisiones durante la transmisión.
* **Detección y corrección de errores**: Mecanismos para identificar y reparar errores que ocurren por ruido, interferencias o fallos en el canal.


**Algunos de los problemas que se pueden encontrar al diseñar una red de comunicación**

* **Interconexión de más de dos elementos: red**  
  > Una red consiste en un conjunto de dispositivos autónomos interconectados que deben comunicarse de forma eficiente.

* **Presentación / Formato del mensaje**  
  Diferencias en la codificación, estructura o representación de los datos que pueden dificultar su interpretación entre sistemas.

* **Seguridad**  
  Riesgos de acceso no autorizado, manipulación o robo de información durante la transmisión.

* **Direccionamiento / Encaminamiento**  
  Necesidad de identificar correctamente el destino de los datos y elegir la mejor ruta para llegar a él.

* **Control de flujo**  
  Mecanismos para evitar que el emisor envíe más datos de los que el receptor puede procesar.

* **Recuperación**  
  Estrategias para restaurar la comunicación o los datos en caso de fallos, pérdidas o interrupciones.

* **Cambios en la estructura o topología de la red**  
  Adaptación ante la incorporación, eliminación o reubicación de dispositivos en la red.

La red puede tener diversos tamaños, y lo conocemos como tipos de redes:
* Local Area Network
* Wide Area Network
* Metropolitan Area Network
* Personal Area Network
* Home Area Network

> [!NOTE] Nota
> La principal razón de una red es compartir hardware y software

Para crear una red se requiere del uso de software, ya que debido a los problemas que tenemos es necesario implementar un conjunto de capas o modulos que ofrezcan servicios.

Debido a la complejidad de la comunicación, esta actividad se divide en tareas, y cada una de ellas se realiza por separado.

Servicios es realizar tareas que le proporciona la capa superior a la capa inferior