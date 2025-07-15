# Tema 10: Algoritmos probabilistas –  (Brassard & Bratley, 2006)

El tema 10 introduce el estudio de los **algoritmos probabilistas**, una clase de algoritmos que hacen uso explícito del azar para tomar decisiones durante su ejecución. A diferencia de los algoritmos deterministas, que siempre producen el mismo resultado dado un mismo conjunto de datos de entrada, los algoritmos probabilistas pueden variar su comportamiento en diferentes ejecuciones, incluso sobre la misma entrada.

Brassard y Bratley explican que el uso de la aleatoriedad no implica pérdida de rigor, sino que ofrece una estrategia poderosa para resolver problemas complejos de forma más eficiente o más sencilla que con enfoques puramente deterministas. En muchos casos, estos algoritmos logran una buena **compensación entre eficiencia y precisión**.

Los autores clasifican los algoritmos probabilistas en dos grandes tipos principales:

1. **Algoritmos de Monte Carlo**: Son algoritmos que tienen un **tiempo de ejecución fijo**, pero cuya **respuesta puede ser incorrecta con una cierta probabilidad**. La ventaja es que suelen ser muy rápidos y, si se diseñan adecuadamente, el error puede hacerse arbitrariamente pequeño repitiendo el experimento. Un ejemplo clásico es el algoritmo de **primalidad de Miller-Rabin**, que determina si un número es primo con una alta probabilidad de acierto, pero no con certeza total.

2. **Algoritmos de Las Vegas**: En este caso, los algoritmos **siempre producen una respuesta correcta**, pero su **tiempo de ejecución es variable** y depende de decisiones aleatorias. Estos algoritmos usan el azar para guiar el proceso de búsqueda, pero garantizan exactitud en el resultado final. Un ejemplo es el algoritmo **Randomized QuickSort**, donde el pivote se elige aleatoriamente para evitar los peores casos típicos del QuickSort clásico.

Los algoritmos probabilistas son especialmente útiles cuando los algoritmos deterministas son demasiado lentos, difíciles de implementar o no se conocen. Además, su análisis se basa en la teoría de la probabilidad, donde se calcula la **esperanza matemática del tiempo de ejecución** o la **probabilidad de éxito**.

Brassard y Bratley hacen énfasis en que muchos problemas complejos o incluso aparentemente intratables pueden abordarse eficazmente con el uso de técnicas aleatorizadas. El uso de la aleatoriedad puede ayudar a evitar patrones desfavorables en los datos o a explorar grandes espacios de soluciones de forma eficiente.

En el capítulo también se destacan ejemplos prácticos como el **algoritmo de verificación de identidades polinómicas** y **algoritmos para encontrar cortes mínimos en grafos**, los cuales muestran que se puede utilizar el azar no solo como recurso técnico, sino como elemento central del diseño algorítmico.

En resumen, este tema demuestra que los algoritmos probabilistas son una herramienta poderosa dentro del diseño algorítmico. Aunque se basan en el azar, pueden ser más rápidos, más simples o más efectivos que sus equivalentes deterministas, especialmente cuando se acepta un margen de error o una variabilidad en el tiempo de ejecución. Los autores concluyen que esta clase de algoritmos merece un lugar fundamental en el repertorio de técnicas que todo diseñador de algoritmos debe dominar.

