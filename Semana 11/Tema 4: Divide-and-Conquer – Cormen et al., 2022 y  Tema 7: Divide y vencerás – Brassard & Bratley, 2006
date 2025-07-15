

# Tema 4: Divide-and-Conquer – *Cormen et al., 2022*

El enfoque de diseño de algoritmos conocido como **Divide and Conquer** (dividir y conquistar) es una de las estrategias fundamentales para resolver problemas algorítmicos de manera eficiente. El principio consiste en **dividir** un problema en subproblemas más pequeños del mismo tipo, **resolver** recursivamente estos subproblemas y luego **combinar** las soluciones para formar la solución al problema original.

Cormen y sus coautores presentan esta técnica como una herramienta poderosa que permite diseñar algoritmos altamente eficientes y formales. La estructura general de un algoritmo "divide y vencerás" sigue tres pasos clave:

1. **Dividir** el problema en uno o más subproblemas más pequeños.
2. **Conquistar** los subproblemas, resolviéndolos de manera recursiva.
3. **Combinar** las soluciones de los subproblemas en una solución del problema original.

El rendimiento de estos algoritmos suele analizarse mediante **relaciones de recurrencia**, que modelan el tiempo de ejecución como una función recursiva del tamaño de entrada. Cormen utiliza el método de sustitución, el método del árbol de recurrencia y el teorema maestro como herramientas para resolver estas recurrencias.

Entre los algoritmos clásicos que se implementan bajo esta estrategia se encuentran:

* **MergeSort**: divide el arreglo a la mitad, ordena recursivamente cada mitad y luego las combina.
* **QuickSort**: selecciona un pivote, divide los elementos en menores y mayores al pivote y aplica recursión.
* **Multiplicación de matrices de Strassen**: divide las matrices en submatrices y reduce el número de multiplicaciones necesarias.
* **Binary Search**: busca un elemento dividiendo el espacio de búsqueda a la mitad en cada paso.

Los autores destacan que "divide y vencerás" es útil cuando el problema original puede reducirse eficientemente a subproblemas independientes. Además, la combinación de las soluciones debe ser computacionalmente menos costosa que la resolución de los subproblemas.

---

# Tema 7: Divide y vencerás – *Brassard & Bratley, 2006*

Brassard y Bratley también abordan el paradigma de **divide y vencerás** como uno de los más fundamentales en el diseño de algoritmos. En su presentación, enfatizan la **recursividad natural** de esta estrategia y la aplicabilidad a problemas que pueden descomponerse en partes más pequeñas de forma estructurada.

El enfoque consiste en dividir el problema en subproblemas más simples, resolverlos de forma recursiva y luego combinar sus soluciones. Lo característico de esta estrategia es que el problema completo debe ser **reducible en subproblemas independientes**, y la solución global debe poder **construirse eficientemente a partir de las soluciones parciales**.

Brassard y Bratley destacan como ejemplos representativos de esta técnica:

* **Ordenación por mezcla (MergeSort)**, que divide un arreglo en dos mitades, ordena recursivamente cada mitad y luego mezcla los resultados.
* **Búsqueda binaria**, que busca dividiendo el intervalo de búsqueda en dos partes y descartando una en cada paso.
* **Multiplicación rápida de enteros grandes**, como en el algoritmo de Karatsuba, que reduce el número de multiplicaciones necesarias dividiendo los operandos.
* **Transformadas rápidas**, como la Transformada Rápida de Fourier (FFT), que aplica esta técnica para acelerar el cálculo de transformadas en procesamiento de señales.

Los autores también explican que muchos algoritmos recursivos que utilizan esta técnica tienen una estructura de recurrencia del tipo:

$$
T(n) = a \cdot T(n/b) + f(n)
$$

donde $a$ es el número de subproblemas generados, $n/b$ es el tamaño de cada subproblema, y $f(n)$ es el costo de dividir y combinar. Esta forma permite analizar el rendimiento usando el **teorema maestro**, el cual clasifica la eficiencia del algoritmo según el crecimiento relativo de $f(n)$ respecto a $n^{\log_b a}$.

Finalmente, Brassard y Bratley subrayan que la estrategia divide y vencerás es especialmente útil en algoritmos que deben procesar grandes cantidades de datos o cuando se necesita dividir tareas para ejecutar en paralelo, haciendo de esta técnica una base no solo en teoría de algoritmos sino también en computación práctica.

---

### Comparación general entre ambos enfoques

| Aspecto                 | Cormen et al. (2022)                               | Brassard & Bratley (2006)                         |
| ----------------------- | -------------------------------------------------- | ------------------------------------------------- |
| Enfoque                 | Formal, enfocado en análisis por recurrencias      | Conceptual, con enfoque en aplicaciones prácticas |
| Herramientas analíticas | Sustitución, árbol de recurrencia, teorema maestro | Teorema maestro, ejemplos estructurados           |
| Ejemplos clásicos       | MergeSort, QuickSort, Binary Search, Strassen      | MergeSort, Binary Search, FFT, Karatsuba          |
| Aplicación destacada    | Análisis riguroso del rendimiento                  | Aplicabilidad estructural y paralelismo           |

---
