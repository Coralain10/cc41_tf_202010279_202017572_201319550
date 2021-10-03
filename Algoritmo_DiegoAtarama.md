# Antes de empezar:
- Se creará la funcion "distancia" y "adyacencia", para la creación de la matriz de adyacencia que se usará en el algoritmo
- Cada nodo tendrá conexión con todos los demás, excepto condigo mismo, y será un grafo simétrico
### Funcion distancia
1. Recibe como parámetros dos puntos
2. Saca los valores x1, x2, y1, y2
3. Retorna la distancia utilizando una formula matemática
### Funcion adyacencia
1. Recibe como parámetros la lista con todos los puntos de distribucion y de entrega
2. Se crea la matríz con ceros
3. Para cada fila i  hacer:
    - Para cada columna j hacer:
        - si j>i, entonces
             - sacar la distancia  del punto en la posicion i de la lista con el punto en la posicion j
            - sacar la gasolina necesaria para la ruta entre los dos puntos
            - Ingresr, en la posicion i,j de la matriz, (distancia, gasolina)
        - si j<i, entonces:
            - Ingresar, en la posicion i,j de la matriz, el valor de la posicion j,i
4. Retornar la matriz

# Algoritmo
El algoritmo utilizará la tecnica de la fuerza bruta, por lo que será un algoritmo extenso, y de gran complejidad. La idea se centra en identificar todos los nodos a los que los que un vehiculo puede llegar gastando la mayor cantidad posible de gasolina que tenga, y habiendo recorrido por lo menos 5 puntos de entrega, no visitados, antes de volver a su punto de distribucion.
Estos 5 o más nodos serán guardados en una lista que sera permutada para hallar todas las rutas posibles para visitar cada nodo y volver al punto de distribución. Entre todas estas rutas, se elegirá la de menor distancia y tiempo, esos datos le corresponderan al vehículo respectivo.
Junto a algunas estructuras condicionales para aplicar ciertas restricciones, este algoritmo se repetirá para cada vehiculo hasta que todos los puntos de entrega hayan sido visitados.
Al final, se mostrara el tiempo y distancia de cada vehículo.
Este algoritmo no garantiza una solución perfecta, pero si una en donde todos los clientes recibiran sus demandas de manera rápida y efectiva.
Al ser una creación propia, aun no cuento con el correcto análisis de complejidad o pseudocódigo.


    
    


