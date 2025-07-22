# Ejemplo algoritmo PRIM
<img width="1600" height="1200" alt="grafo_prim" src="https://github.com/user-attachments/assets/478dff28-9fcf-4639-a585-1e425b37032b" />


##  Código Java – Algoritmo de Prim

```java
import java.util.*;

public class AlgoritmoPrim {
    static class Arista {
        int destino, peso;

        Arista(int destino, int peso) {
            this.destino = destino;
            this.peso = peso;
        }
    }

    static void prim(List<List<Arista>> grafo, int inicio) {
        int V = grafo.size();
        boolean[] visitado = new boolean[V];
        int[] padre = new int[V];
        int[] clave = new int[V];

        Arrays.fill(clave, Integer.MAX_VALUE);
        clave[inicio] = 0;
        padre[inicio] = -1;

        PriorityQueue<int[]> cola = new PriorityQueue<>(Comparator.comparingInt(a -> a[1]));
        cola.offer(new int[]{inicio, 0});

        while (!cola.isEmpty()) {
            int u = cola.poll()[0];
            visitado[u] = true;

            for (Arista arista : grafo.get(u)) {
                int v = arista.destino;
                int peso = arista.peso;

                if (!visitado[v] && peso < clave[v]) {
                    clave[v] = peso;
                    padre[v] = u;
                    cola.offer(new int[]{v, clave[v]});
                }
            }
        }

        System.out.println("Aristas del árbol de expansión mínima:");
        int total = 0;
        for (int i = 0; i < V; i++) {
            if (padre[i] != -1) {
                System.out.println(padre[i] + " - " + i + " (peso: " + clave[i] + ")");
                total += clave[i];
            }
        }
        System.out.println("Costo total: " + total);
    }

    public static void main(String[] args) {
        int V = 4; // A, B, C, D => 0,1,2,3
        List<List<Arista>> grafo = new ArrayList<>();
        for (int i = 0; i < V; i++) grafo.add(new ArrayList<>());

        // A-B (5), A-C (1), A-D (3), B-C (4), C-D (2)
        grafo.get(0).add(new Arista(1, 5)); grafo.get(1).add(new Arista(0, 5));
        grafo.get(0).add(new Arista(2, 1)); grafo.get(2).add(new Arista(0, 1));
        grafo.get(0).add(new Arista(3, 3)); grafo.get(3).add(new Arista(0, 3));
        grafo.get(1).add(new Arista(2, 4)); grafo.get(2).add(new Arista(1, 4));
        grafo.get(2).add(new Arista(3, 2)); grafo.get(3).add(new Arista(2, 2));

        prim(grafo, 0); // Comienza desde A (índice 0)
    }
}
```

---

##  Prueba de escritorio (Paso a paso)

| Paso | Nodo actual | Aristas disponibles        | Arista elegida | Nuevos visitados | Costo acumulado |
| ---- | ----------- | -------------------------- | -------------- | ---------------- | --------------- |
| 1    | A (0)       | A-B(5), A-C(1), A-D(3)     | A-C (1)        | A, C             | 1               |
| 2    | C (2)       | C-B(4), C-D(2)             | C-D (2)        | A, C, D          | 3               |
| 3    | D (3)       | D-A(3), D-C(2) – ignoradas |                |                  |                 |
| 4    | B (1)       | B-C(4), B-A(5) – ignoradas | C-B (4)        | A, B, C, D       | 7               |

 **Árbol generado**:

* A-C (1)
* C-D (2)
* C-B (4)

🎯 **Costo total:** 7

---

