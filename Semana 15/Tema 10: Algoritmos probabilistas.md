# Tema 10: Algoritmos probabilistas – *Resumen (Brassard & Bratley, 2006)*

En este capítulo, Brassard y Bratley introducen los **algoritmos probabilistas** como una clase de algoritmos que utilizan el azar como parte de su lógica interna. A diferencia de los algoritmos deterministas, donde el resultado depende únicamente de la entrada, los algoritmos probabilistas pueden generar distintos comportamientos en diferentes ejecuciones sobre la misma entrada, debido al uso de decisiones aleatorias durante su ejecución.

Los autores explican que la aleatoriedad puede ser una herramienta útil cuando se busca mejorar el tiempo de ejecución, simplificar un algoritmo o abordar problemas para los que no se conocen soluciones deterministas eficientes. En lugar de ver el azar como una debilidad, los algoritmos probabilistas lo incorporan estratégicamente para obtener soluciones eficientes o para sortear casos desfavorables de entrada.

El capítulo distingue entre dos tipos principales de algoritmos probabilistas:

1. **Algoritmos de Monte Carlo**: Son algoritmos que **tienen tiempo de ejecución acotado**, pero cuya **respuesta puede ser incorrecta con cierta probabilidad**. Es decir, pueden dar una respuesta errónea, pero se conoce la probabilidad de fallo y esta puede reducirse con repeticiones. Este tipo de algoritmos es útil cuando se necesita rapidez, y se está dispuesto a aceptar un pequeño margen de error. Un ejemplo importante es el **test de primalidad de Miller-Rabin**, que verifica si un número es primo con alta probabilidad de acierto. A pesar de que la respuesta puede ser incorrecta, en la práctica el error puede hacerse tan pequeño como se desee.

2. **Algoritmos de Las Vegas**: Son algoritmos que **siempre devuelven una respuesta correcta**, pero cuyo **tiempo de ejecución depende del azar**. En este caso, el algoritmo nunca se equivoca, pero puede tardar más o menos en completarse según las elecciones aleatorias que haga durante su ejecución. Un ejemplo claro es la versión aleatorizada de QuickSort, donde el pivote se elige aleatoriamente. Aunque el peor caso sigue siendo posible, la elección aleatoria reduce significativamente su ocurrencia.

Brassard y Bratley destacan que los algoritmos probabilistas pueden ser más fáciles de diseñar que los algoritmos deterministas equivalentes, y que en muchos casos son más eficientes, sobre todo cuando el comportamiento promedio importa más que el peor caso. También explican que el análisis de este tipo de algoritmos involucra conceptos de probabilidad como esperanza matemática, varianza y probabilidad de éxito, lo que requiere un enfoque diferente al análisis tradicional.

Un aspecto importante que se menciona es que algunos algoritmos probabilistas pueden convertirse en deterministas si se dispone de una fuente de "aleatoriedad perfecta", o mediante técnicas de eliminación del azar conocidas como *derandomización*. Sin embargo, muchas veces se prefiere mantener la aleatoriedad debido a la simplicidad y eficacia que aporta al diseño del algoritmo.

Finalmente, los autores discuten ejemplos representativos que muestran la efectividad de este enfoque, como algoritmos para verificación de identidades polinómicas, simulaciones numéricas y problemas de grafos. Estos ejemplos ilustran cómo el uso controlado del azar puede hacer posibles soluciones rápidas y prácticas para problemas que de otro modo serían demasiado costosos o complejos.

En conclusión, los algoritmos probabilistas representan una herramienta poderosa dentro del diseño algorítmico. No solo amplían el repertorio de técnicas disponibles, sino que también permiten abordar problemas difíciles de manera ingeniosa y eficiente. Brassard y Bratley argumentan que, si se analiza y controla correctamente la probabilidad de error, el enfoque probabilista es completamente válido, riguroso y útil en la práctica.

---

