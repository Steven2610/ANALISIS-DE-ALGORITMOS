

## 📘 PRIMERA PARTE:

**Dado:**

* $f(n) = n^3 + 9n^2 \log(n)$
* $g(n) = n^2 \log(n)$

### 🔹 ¿Es $f(n) \in \mathcal{O}(g(n))$?

Buscamos si existe una constante $c > 0$ y un valor $n_0$ tal que:

$$
f(n) \leq c \cdot g(n) \quad \text{para todo } n \geq n_0
$$

Sustituimos:

$$
n^3 + 9n^2 \log(n) \leq c \cdot n^2 \log(n)
\Rightarrow
\underbrace{n^3}_{\text{domina}} + 9n^2 \log(n) \leq c \cdot n^2 \log(n)
$$

Dividimos ambos lados entre $n^2 \log(n)$:

$$
\frac{n^3}{n^2 \log(n)} + 9 \leq c
\Rightarrow
\frac{n}{\log(n)} + 9 \leq c
$$

Pero sabemos que:

$$
\lim_{n \to \infty} \frac{n}{\log(n)} = \infty
\Rightarrow
\frac{n}{\log(n)} + 9 \to \infty
$$

🔴 **No existe una constante `c` tal que cumpla la desigualdad**, entonces:

$$
\boxed{f(n) \notin \mathcal{O}(g(n))}
$$

---

### 🔹 ¿Es $f(n) \notin \mathcal{O}(n^2)$?

Sí, vamos a probarlo formalmente.

$$
f(n) = n^3 + 9n^2 \log(n)
\quad \text{y} \quad h(n) = n^2
$$

Dividimos:

$$
\frac{f(n)}{h(n)} = \frac{n^3 + 9n^2 \log(n)}{n^2}
= n + 9 \log(n)
\to \infty \text{ cuando } n \to \infty
$$

Por tanto:

$$
\boxed{f(n) \notin \mathcal{O}(n^2)}
$$

---

## 📗 SEGUNDA PARTE:

**Dado:**

* $f(n) = 2^n$
* $g(n) = 2^{2n} = (2^n)^2$

---

### 🔹 ¿$f(n) \in \mathcal{O}(g(n))$?

Sí. Porque:

$$
\frac{f(n)}{g(n)} = \frac{2^n}{2^{2n}} = 2^{-n} \to 0
\Rightarrow f(n) = o(g(n)) \Rightarrow f(n) \in \mathcal{O}(g(n))
$$

✅ **Sí pertenece**:

$$
\boxed{f(n) \in \mathcal{O}(g(n))}
$$

---

### 🔹 ¿$g(n) \in \mathcal{O}(f(n))$?

No. Porque:

$$
\frac{g(n)}{f(n)} = \frac{2^{2n}}{2^n} = 2^n \to \infty
\Rightarrow g(n) \notin \mathcal{O}(f(n))
$$

🔴 **No pertenece**:

$$
\boxed{g(n) \notin \mathcal{O}(f(n))}
$$

---

## ✅ CONCLUSIÓN GENERAL:

| Relación                                                        | Resultado      |
| --------------------------------------------------------------- | -------------- |
| $f(n) = n^3 + 9n^2 \log(n) \in \mathcal{O}(g(n)) = n^2 \log(n)$ | ❌ No pertenece |
| $f(n) \notin \mathcal{O}(n^2)$                                  | ✅ Confirmado   |
| $f(n) = 2^n \in \mathcal{O}(2^{2n})$                            | ✅ Sí pertenece |
| $g(n) = 2^{2n} \in \mathcal{O}(2^n)$                            | ❌ No pertenece |

---

