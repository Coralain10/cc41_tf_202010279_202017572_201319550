# Vecino más cercano
El algoritmo a considerar es el del vecino más cercano.
Consiste en 1) visitar un nodo, el cual se agrega a la lista del camino acumulado, y
y 2) encontrar, entre todos los nodos vecinos no visitados, al de menor costo,
luego agregarlo al camino acumulado y sumar el costo entre nodos al costo del camino. 
Se repite en bucle encontrar al nodo más cercano (2) hasta que todos los nodos hayan sido visitados.
Cuando se llega a este último nodo, se vuelve al nodo inicial y se aumenta el costo entre ambos nodos.

Como se observa, no es un algoritmo completamente eficiente en el sentido en el que
no "mira hacia el futuro", es decir, es posible que la distancia entre el último y primer nodo sea de gran longitud.
Asimismo, el resultado también variará dependiendo de cuál nodo se elija primero para recorrer.
Para solucionar ello, se puede considerar repetir este algoritmo por cada nodo y elegir el que retorne el menor peso.
Sin embargo, debido a la magnitud de los datos a considerar, ello podría ser inviable.

## Restricciones
Dado que hallar una sola ruta entre todos los nodos del caso es ineficiente,
dado que hay diferentes puntos de distribución en el mapa,
se consideran algunas restricciones:

1. Deberá indicarse una distancia máxima entre nodos.
  * Una opción es usar como distancia máxima el promedio de los de distancias entre los nodos de distribución.
  * Otra opción es buscar el vecino más cercano al nodo de distribución actual.
 Sin embargo, este recorrido incrementa aún más el tiempo de búsqueda, ya que se repite por cada nodo de distribución.
3. La distancia entre nodos de entrega deberá ser menor o igual a la distancia máxima entre nodos
  * Ello permite mantener reducir las posibilidades de agrupación de nodos y disminuir las distancias.

## Complejidad algorítmica
Se estima que el algoritmo debería tener una complejidad menor a
<img src="https://latex.codecogs.com/svg.latex?1+log(n)/2" /> 

## Referencias
1. [RdV - 1.3: Heurísticas para el TSP](https://youtu.be/EJbV3GUOQHY?t=169)
2. [Nearest Neighbour - Heurística el Vecino más cercano](https://www.youtube.com/watch?v=vKRgagilzT8&t=534s&ab_channel=sergiocorrea) 
