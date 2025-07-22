---

##  Código completo en Java

```java
public class GeneradorPseudoaleatorio {

    public static double[] generarPseudoaleatorios(long semilla, int cantidad) {
        // Parámetros del generador (Numerical Recipes)
        long a = 1664525;
        long c = 1013904223;
        long m = (long) Math.pow(2, 32);

        double[] resultados = new double[cantidad];
        long x = semilla;

        for (int i = 0; i < cantidad; i++) {
            x = (a * x + c) % m;
            resultados[i] = (double) x / m; // Normalización en [0, 1]
        }

        return resultados;
    }

    public static void main(String[] args) {
        int cantidad = 10;
        long semilla = 12345;

        double[] numeros = generarPseudoaleatorios(semilla, cantidad);

        System.out.println("Números pseudoaleatorios generados:");
        for (double num : numeros) {
            System.out.println(num);
        }
    }
}
```

---

##  Prueba de escritorio (paso a paso con los primeros 3 números)

### Parámetros:

* `a = 1664525`
* `c = 1013904223`
* `m = 2^32 = 4294967296`
* `semilla = 12345`


---


---

### 🧪 Tabla: Iteración paso a paso

| Iteración | $x_i$      | Cálculo $x_{i+1} = (a \cdot x_i + c) \mod m$      | $x_{i+1}$  | $r_i = x_{i+1}/m$ |
| --------- | ---------- | ------------------------------------------------- | ---------- | ----------------- |
| 0         | 12345      | $(1664525 × 12345 + 1013904223) \mod 2^{32}$      | 87628868   | 0.0204            |
| 1         | 87628868   | $(1664525 × 87628868 + 1013904223) \mod 2^{32}$   | 71072467   | 0.0165            |
| 2         | 71072467   | $(1664525 × 71072467 + 1013904223) \mod 2^{32}$   | 2332836370 | 0.5432            |
| 3         | 2332836370 | $(1664525 × 2332836370 + 1013904223) \mod 2^{32}$ | 2726892157 | 0.6351            |
| 4         | 2726892157 | $(1664525 × 2726892157 + 1013904223) \mod 2^{32}$ | 3908547000 | 0.9100            |

---

### ✅ Conclusión

Cada número generado:

* Se basa en el anterior, usando multiplicación, suma y módulo.
* Se normaliza dividiendo entre $m$ para obtener un valor entre 0 y 1.


