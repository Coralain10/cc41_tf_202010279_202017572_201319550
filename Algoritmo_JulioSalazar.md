# Idea de algoritmo:
El algoritmo se basa en realizar una iteracion por cada nodo y almacenar el camino con menor distancia del mismo, cambiando el estado de cada nodo del camino agregado a nivel 1(conectado a sun solo nodo, el limite es 2). Se priorizara que la siguiente iteracion sea en otro nodo de nivel 0, con el fin de no realizar algo similar al algoritmo del vecino más proximo. Por otro lado, cuando no exista mas nodos nivel 0, los nodos de nivel 1 se insertaran al siguiente nodo nivel 1 con menor distancia creando asi una ruta hasta que todos los caminos agregados anteriormente por orden de distancia esten conectados. Por ultimo, se considera que la distancia de la ruta debe ser menor o igual a la distancia que puede realizar el vehiculo con el combustible que incia su viaje, en su defecto se eliminara el nodo mas lejano al origen y se uniran los nodos de nivel 1 restantes. 

## Terminos a tener en cuenta:
* Un camino es la conexion entre 2 nodos solamente.
* La ruta es el resultado de la conexion de todos los caminos, por ende todos los nodos.
* Se implementara un metodo que retorne el nodo destino con menor distancia del nodo origen enviado por parametro.
* Se almacenara los caminos en orden considerando distancia entre los nodos que lo conforman.

## Conclusion:
El algoritmo realizara la construccion de la ruta de forma secuencial agregando caminos desde el mas corto al mas largo entre si, teniendo en cuenta la distancia que puede recorrer el vehiculo designado por la cantidad de combustible que inicia.  
