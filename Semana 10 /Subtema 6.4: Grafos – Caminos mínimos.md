

# Subtema 6.4: Grafos – Caminos mínimos 

El subtema 6.4 se enfoca en la aplicación de algoritmos voraces para resolver el problema de **caminos mínimos en grafos ponderados**, es decir, encontrar la ruta de costo mínimo entre un nodo origen y los demás nodos de un grafo. Brassard y Bratley presentan como caso central el **algoritmo de Dijkstra**, un algoritmo voraz clásico que permite resolver este problema cuando **los pesos de las aristas son no negativos**.

El objetivo del algoritmo de Dijkstra es determinar el camino más corto desde un nodo fuente a todos los demás nodos de un grafo dirigido o no dirigido. La estrategia voraz que utiliza consiste en mantener un conjunto de nodos a los cuales ya se conoce la distancia mínima desde el origen, e ir expandiendo este conjunto eligiendo, en cada paso, el nodo con la **distancia mínima más cercana** entre los aún no procesados. Esta elección es localmente óptima y se basa en la suposición de que avanzar hacia los nodos más cercanos primero conduce a una solución global óptima.

El algoritmo se apoya en una estructura de datos que permite gestionar eficientemente los nodos aún no visitados, como una cola de prioridad, lo cual mejora su rendimiento. En cada iteración, el algoritmo extrae el nodo con menor costo acumulado y actualiza las distancias de sus vecinos si se encuentra un camino más corto a través del nodo actual. Este proceso continúa hasta que todos los nodos han sido procesados o hasta encontrar el camino más corto hacia un nodo destino particular.

El algoritmo de Dijkstra cumple con las condiciones necesarias para aplicar un enfoque voraz: la **subestructura óptima**, porque los caminos mínimos hacia los subnodos del destino forman parte del camino mínimo total; y la **propiedad de elección voraz**, porque siempre es seguro elegir el nodo más cercano no procesado en cada paso, dado que no hay aristas con peso negativo.

Sin embargo, Brassard señala que este algoritmo **no es adecuado para grafos con pesos negativos**, ya que suposiciones clave del enfoque voraz se rompen en ese caso. Para estos casos se requiere un enfoque diferente, como el **algoritmo de Bellman-Ford**, que no es voraz sino iterativo y basado en programación dinámica.

En resumen, el subtema 6.4 demuestra cómo el algoritmo de Dijkstra es una aplicación exitosa del paradigma voraz en problemas de caminos mínimos, siempre que las condiciones del problema lo permitan. Su eficiencia y simplicidad lo convierten en una herramienta fundamental en teoría de grafos y en aplicaciones prácticas como redes de computadoras, navegación y transporte.

