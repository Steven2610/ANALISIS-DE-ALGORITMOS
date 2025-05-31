

##  Tema 3: Notación Asintótica

**Referencia**: Brassard, G. & Bratley, P. (2006). *Fundamentals of Algorithmics*. Tema 3: Notación Asintótica.

### Introducción

La notación asintótica proporciona una forma matemática precisa para describir cómo crece el tiempo de ejecución o el uso de memoria de un algoritmo en función del tamaño de entrada $n$. Es un lenguaje fundamental para el análisis de algoritmos, ya que permite comparar la eficiencia de diferentes soluciones.
 

### Notaciones principales

#### 1. **Notación O grande** — *Cota superior asintótica*

Describe un límite superior para el crecimiento de una función.
Se dice que:

$$
f(n) \in O(g(n))
$$

si existen constantes $c > 0$ y $n_0$ tal que:

$$
f(n) \leq c \cdot g(n) \quad \text{para todo } n \geq n_0
$$

> **Uso:** Describe el *peor caso* o el *rendimiento máximo esperado*.

---

#### 2. **Notación Ω grande** — *Cota inferior asintótica*

Define un límite inferior del crecimiento.
Se dice que:

$$
f(n) \in \Omega(g(n))
$$

si existen constantes $c > 0$ y $n_0$ tal que:

$$
f(n) \geq c \cdot g(n) \quad \text{para todo } n \geq n_0
$$

> **Uso:** Garantiza que el algoritmo *al menos* consume ese tiempo.

---

#### 3. **Notación Θ grande** — *Cota ajustada asintótica*

Significa que la función está acotada por arriba y por abajo por la misma expresión.

$$
f(n) \in \Theta(g(n))
$$

si existen constantes $c_1, c_2 > 0$ y $n_0$ tal que:

$$
c_1 \cdot g(n) \leq f(n) \leq c_2 \cdot g(n) \quad \text{para todo } n \geq n_0
$$

> **Uso:** Representa el *comportamiento exacto* del algoritmo a gran escala.

---

### Reglas de cálculo comunes

* Constantes se ignoran: $O(3n) = O(n)$
* Se descartan términos menores: $O(n^2 + n) = O(n^2)$
* Producto de funciones: $O(n) \cdot O(\log n) = O(n \log n)$

---

### Comparación de funciones por crecimiento

Del más lento al más rápido:

$$
1 < \log n < n < n \log n < n^2 < 2^n < n!
$$

Esta jerarquía permite saber qué algoritmos escalan mejor cuando crece la entrada.

---

## 🛠️ Desarrollo de casos de análisis de algoritmos

### Caso 1: Algoritmo de Búsqueda Lineal

```java
int buscar(int[] A, int x) {
  for (int i = 0; i < A.length; i++) {
    if (A[i] == x)
      return i;
  }
  return -1;
}
```

* **Mejor caso**: $O(1)$ (el elemento está en la primera posición).
* **Peor caso**: $O(n)$ (el elemento no está o está al final).
* **Caso promedio**: $O(n)$

---

### Caso 2: Algoritmo de Ordenamiento Burbuja

```java
for (int i = 0; i < n; i++) {
  for (int j = 0; j < n - i - 1; j++) {
    if (A[j] > A[j+1]) {
      intercambiar(A, j, j+1);
    }
  }
}
```

* **Mejor caso**: $O(n)$ (si se optimiza con bandera de intercambio).
* **Peor caso**: $O(n^2)$
* **Caso promedio**: $O(n^2)$

---

### Caso 3: Búsqueda Binaria

```java
int buscarBin(int[] A, int x) {
  int izq = 0, der = A.length - 1;
  while (izq <= der) {
    int mid = (izq + der) / 2;
    if (A[mid] == x) return mid;
    if (A[mid] < x) izq = mid + 1;
    else der = mid - 1;
  }
  return -1;
}
```

* **Requiere array ordenado**
* **Complejidad en todos los casos**: $O(\log n)$

---


