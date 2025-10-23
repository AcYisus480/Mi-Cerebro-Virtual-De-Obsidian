___

***Falta***
#### Falta información



___

### Capa de red
Un enrutador posee básicamente dos funciones:
* Reenvío.
  *Acción de encaminar al paquete a su destino*
* Enrutamiento.
  *Determinar que camino tiene que tomar el paquete para llegar a su destino*
	* Hace la función de enrutamiento, (busca los camino y elige el mas adecuado, esto usando un algoritmo).

***Algoritmo de enrutamiento:*** decide cuál será la línea de salida que seguirá un paquete transmitido. Su característica principal es que debe ser capaz de manejar los cambios de la topología y del tráfico en una red.

Sin embargo, conocer los posibles caminos o rutas en una red no es el único problema, también: 
* Una vez construida la “tabla de caminos”, ¿Qué búsqueda es la más optima en la tabla?
* Si la “tabla de caminos” no es estática, ¿Cómo deberá ser la actualización? 
* Si una tabla es dinamica, esto consiste en que esta tabla cambia constantemente en el tiempo. Aquí es necesario ejecutar el algoritmo de enrutamiento cada cierto tiempo.

El algoritmo de enrutamiento actualiza la tabla de caminos, pero no especifica el tiempo de actualización.

Propiedades de los algoritmos de enrutamiento:
* Entrega rápida y precisa de los paquetes: 
	* El paquete tiene que llegar a su destino sin problemas (***Exactitud***).
* Adaptabilidad a los cambios de la topología de la red: robustez.
	* El algoritmo de enrutamiento tiene que detectar los cambios de la topología.
* Alcanzar el equilibrio: estabilidad.
* Equitativo y óptimo.
	* Elegir rutas para evitar congestión.


Los algoritmos de enrutamiento se clasifican en:
* Adaptativos.
	* Lanzados periodicamente para detectar los caminos.
* No adaptativos. 
	* Llenan información de las tablas solo por una ocasión, en este caso es por que los proveedores no cambiaran la topología.

***Principio de optimización:*** Si un enrutador J está en una ruta óptima del enrutador I al K, entonces la ruta óptima de J a K también está en la misma ruta.



