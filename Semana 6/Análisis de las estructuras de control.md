



## **Resumen: 4.2 Análisis de las estructuras de control**

**Referencia**: Brassard, G., & Bratley, P. (2000). *Fundamentals of Algorithmics*, sección 4.2, págs. 111–117.

### Contexto general

El análisis de algoritmos no solo depende de la comprensión del crecimiento asintótico de funciones, sino también del impacto que tienen **las estructuras de control básicas** (como secuencias, condicionales e iteraciones) sobre el tiempo de ejecución. Brassard y Bratley dedican esta sección a explicar cómo analizar estas estructuras y cómo modelar el tiempo que toma un algoritmo al ejecutarse, considerando la complejidad individual de sus componentes.

### 1. **Secuencias (Sequence)**

Una secuencia de instrucciones se analiza sumando los tiempos de ejecución individuales de cada una. Si una instrucción toma $T_1(n)$ y otra $T_2(n)$, la complejidad total es:

$$
T(n) = T_1(n) + T_2(n)
$$

**Ejemplo**:

```pseudo
x ← A[i]
y ← B[j]
z ← x + y
```

Cada instrucción es constante ($O(1)$), por lo tanto, la complejidad total es $O(1)$.

### 2. **Condicionales (If...Then...Else)**

Para una estructura condicional, se analiza el tiempo de ejecución de **cada rama** y se toma la más costosa (caso peor). Si el bloque "then" tiene costo $T_1(n)$ y el bloque "else" tiene $T_2(n)$, entonces:

$$
T(n) = \max(T_1(n), T_2(n))
$$

Este análisis es esencial porque, en muchos algoritmos, una decisión puede llevar a caminos de ejecución con costos muy diferentes.

### 3. **Iteraciones (Bucles / Loops)**

La estructura **más importante** en el análisis algorítmico. Se considera el número de veces que se ejecuta el bucle y el costo de su cuerpo.

#### a) **Bucles For**

Cuando el número de iteraciones está claramente definido (por ejemplo, de $i = 1$ a $n$), se multiplica el número de iteraciones por el costo del cuerpo del bucle.

$$
T(n) = \sum_{i=1}^{n} T_{\text{cuerpo}}(i)
$$

Si el cuerpo tiene costo constante: $T(n) = O(n)$
Si el cuerpo tiene un costo que depende de $i$, se usa la suma correspondiente.

#### b) **Bucles While / Repeat Until**

Son más difíciles de analizar porque su número de iteraciones no siempre es evidente. Se requiere estimar una **función de progreso**, una medida que decrece en cada iteración y asegura la terminación del bucle.

Ejemplo:

```pseudo
while n > 1 do
    n ← n / 2
```

Este bucle ejecuta un número de veces proporcional a $\log n$, por lo tanto, su complejidad es $O(\log n)$.

#### c) **Bucles anidados (Nested loops)**

En bucles anidados, el número total de operaciones es el producto del número de iteraciones de cada nivel. Por ejemplo:

```pseudo
for i ← 1 to n do
   for j ← 1 to n do
       A[i][j] ← 0
```

Este fragmento tiene complejidad $O(n^2)$ ya que hay $n \times n$ operaciones.

---

### Consideraciones adicionales del análisis

* Se analiza siempre en función del tamaño de la entrada $n$.
* Es importante **identificar el caso peor**, aunque también se pueden analizar el **caso promedio** o el **mejor caso**.
* La notación asintótica (O, Ω, Θ) sigue aplicándose a las estructuras de control para resumir su comportamiento.

---

### Conclusión

El análisis de estructuras de control es esencial para descomponer algoritmos complejos en partes manejables. Comprender cómo se comporta cada tipo de estructura permite estimar de forma precisa la eficiencia global del algoritmo y tomar decisiones informadas sobre optimización.


