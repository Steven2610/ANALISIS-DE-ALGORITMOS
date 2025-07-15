
# Tema 6: Algoritmos Voraces (Resumen)

Los algoritmos voraces representan una estrategia de diseño algorítmico que consiste en construir soluciones a problemas de manera progresiva, eligiendo en cada paso la opción que parece ser la mejor en ese momento. Esta estrategia se caracteriza por realizar elecciones locales óptimas con la esperanza de que, al final del proceso, estas decisiones conduzcan a una solución globalmente óptima. La clave de este enfoque es que las decisiones tomadas en un paso no se revierten posteriormente.

Un algoritmo voraz funciona bien solo para ciertos tipos de problemas, y su éxito depende de dos condiciones fundamentales: la **subestructura óptima** y la **propiedad de elección voraz**. La subestructura óptima implica que una solución óptima para un problema contiene soluciones óptimas para sus subproblemas. Por otro lado, la propiedad de elección voraz asegura que tomar una decisión local óptima en cada paso conduce a la solución óptima global.

La estructura general de un algoritmo voraz se basa en definir un conjunto de candidatos, una función que permita seleccionar el mejor candidato en cada paso, una función de factibilidad para verificar si una solución parcial sigue siendo válida, y una función objetivo que mide la calidad de una solución. El algoritmo comienza con una solución vacía y, mientras haya candidatos disponibles, selecciona el mejor de acuerdo con un criterio específico y lo incluye en la solución si se mantiene la factibilidad.

Entre los ejemplos clásicos de algoritmos voraces se encuentran el problema de la **mochila fraccional**, el **problema del cambio de monedas**, los algoritmos de **árbol de expansión mínima** como los de **Prim y Kruskal**, y la **codificación de Huffman**. En el caso de la mochila fraccional, donde se permite tomar fracciones de los objetos, el algoritmo voraz proporciona una solución óptima. Por el contrario, en el problema del cambio de monedas, el enfoque voraz puede fallar si las denominaciones no permiten formar cualquier cantidad de forma óptima con las monedas más grandes primero.

En los algoritmos de Prim y Kruskal, que buscan construir un árbol de expansión mínima a partir de un grafo conexo, el enfoque voraz es adecuado porque las decisiones locales (selección de aristas de menor peso sin formar ciclos) conducen a una solución óptima. De forma similar, el algoritmo de codificación de Huffman genera una codificación binaria óptima para un conjunto de caracteres, basándose en su frecuencia, mediante la combinación iterativa de los caracteres menos frecuentes.

Aunque los algoritmos voraces son generalmente más simples y eficientes que otros enfoques como la **programación dinámica**, no siempre garantizan la obtención de una solución óptima. La programación dinámica, por su parte, también se basa en la subestructura óptima, pero no requiere la propiedad de elección voraz, y es capaz de encontrar la solución óptima incluso en problemas donde los algoritmos voraces fallan.

La siguiente tabla resume las diferencias clave entre los algoritmos voraces y la programación dinámica:

| Característica                | Algoritmos Voraces             | Programación Dinámica      |
| ----------------------------- | ------------------------------ | -------------------------- |
| Estrategia                    | Elección local óptima          | Resolución de subproblemas |
| Requiere subestructura óptima | Sí                             | Sí                         |
| Requiere propiedad voraz      | Sí                             | No                         |
| Complejidad computacional     | Baja (eficiente)               | Moderada o alta            |
| Garantiza solución óptima     | Solo si se cumplen condiciones | Sí (si aplica el enfoque)  |

En conclusión, los algoritmos voraces ofrecen soluciones eficientes y de implementación sencilla, pero su aplicación exitosa depende de que el problema cumpla con ciertas propiedades. Brassard y Bratley enfatizan que se debe analizar cuidadosamente la estructura del problema antes de optar por este enfoque, y, en caso de duda, se recomienda contrastar los resultados con técnicas más robustas como la programación dinámica o el backtracking.

