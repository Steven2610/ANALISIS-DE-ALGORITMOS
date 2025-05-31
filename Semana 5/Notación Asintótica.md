

# Resumen: Notación Asintótica (Brassard y Bratley, 2006)

La notación asintótica es una herramienta matemática fundamental utilizada en el análisis de algoritmos para describir su eficiencia en función del tamaño de la entrada. Su propósito principal es caracterizar el crecimiento de una función que representa el tiempo de ejecución o el uso de recursos (como espacio en memoria) conforme la entrada del algoritmo se hace arbitrariamente grande.

Brassard y Bratley, en su libro *Fundamentals of Algorithmics* (2006), presentan este tipo de notación como una forma de clasificar algoritmos según su comportamiento de rendimiento, independientemente de implementaciones específicas, detalles del lenguaje de programación o del hardware utilizado. Se enfocan en el orden de crecimiento, lo que permite realizar comparaciones abstractas y generalizadas entre algoritmos.

### Tipos principales de notación asintótica

#### 1. **Notación O (O grande)**

Representa un **límite superior** del comportamiento de una función. Se utiliza para describir la **peor complejidad posible** de un algoritmo, es decir, la cantidad máxima de recursos que podría requerir en el peor caso.

Formalmente, se dice que una función $f(n) \in O(g(n))$ si existen constantes positivas $c$ y $n_0$ tales que:

$$
f(n) \leq c \cdot g(n) \quad \text{para todo } n \geq n_0
$$

Esta notación abstrae los detalles menores y se enfoca en el término de crecimiento dominante.

#### 2. **Notación Ω (Omega)**

Proporciona un **límite inferior** al crecimiento de una función. Describe el **mejor caso posible** de un algoritmo o el mínimo de recursos que siempre necesitará a medida que el tamaño de entrada crece.

Se dice que $f(n) \in \Omega(g(n))$ si existen constantes positivas $c$ y $n_0$ tales que:

$$
f(n) \geq c \cdot g(n) \quad \text{para todo } n \geq n_0
$$

Esta notación asegura que el algoritmo **nunca** será más rápido (en orden de crecimiento) que lo indicado por $g(n)$.

#### 3. **Notación Θ (Theta)**

Se utiliza para dar una **cota exacta** (tanto superior como inferior) del comportamiento de una función. Se dice que $f(n) \in \Theta(g(n))$ si existen constantes positivas $c_1, c_2$ y $n_0$ tales que:

$$
c_1 \cdot g(n) \leq f(n) \leq c_2 \cdot g(n) \quad \text{para todo } n \geq n_0
$$

Cuando se cumple esta relación, se afirma que $g(n)$ es una estimación precisa del crecimiento de $f(n)$, lo que significa que el algoritmo es tan rápido (o lento) como $g(n)$ en el orden asintótico.

### Importancia en el análisis de algoritmos

El uso de la notación asintótica permite a los diseñadores de algoritmos:

* Comparar algoritmos en cuanto a su eficiencia de forma independiente de factores externos.
* Predecir el rendimiento de los algoritmos en entradas grandes.
* Identificar cuellos de botella y oportunidades de optimización.
* Comunicar de manera estandarizada el rendimiento algorítmico dentro de la comunidad científica.

### Ejemplos

* Si un algoritmo tiene una complejidad de tiempo $T(n) = 3n^2 + 4n + 1$, se dice que su orden de crecimiento es $O(n^2)$, ya que el término cuadrático domina para valores grandes de $n$.
* Un algoritmo de búsqueda lineal en una lista no ordenada tiene complejidad $\Theta(n)$.
* Un algoritmo de ordenamiento como merge sort tiene complejidad $\Theta(n \log n)$.

