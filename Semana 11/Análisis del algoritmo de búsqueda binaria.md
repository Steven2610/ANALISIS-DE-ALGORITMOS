---

#  Búsqueda Binaria


![WhatsApp Image 2025-07-22 at 11 24 47 AM (3)](https://github.com/user-attachments/assets/fa0172c2-cce4-45d2-bf83-280f7c429c4c)


---
Dado el arreglo:
`t[] = [8, 12, 20, 24, 28, 30, 38, 42, 50]`
Buscar: `x = 12`
Tamaño del arreglo: `n = 9`

---

###  Prueba de escritorio paso a paso

Usamos la fórmula:

```
mid = (low + high) / 2
```

#### Inicialización:

* `low = 0`
* `high = 8`
* `x = 12`

| Paso | low | high | mid | t\[mid] | Comparación | Acción                     |
| ---- | --- | ---- | --- | ------- | ----------- | -------------------------- |
| 1    | 0   | 8    | 4   | 28      | 12 < 28     | high = mid - 1 = 3         |
| 2    | 0   | 3    | 1   | 12      | 12 == 12    |  Encontrado en posición 1 |

**Resultado:** Se encontró `12` en la **posición 1** del arreglo.

---

##  Código Java – Búsqueda Binaria

```java
public class BusquedaBinaria {
    public static int busquedaBinaria(int[] t, int x) {
        int low = 0;
        int high = t.length - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (t[mid] == x) {
                return mid; // Elemento encontrado
            } else if (t[mid] < x) {
                low = mid + 1; // Buscar en la derecha
            } else {
                high = mid - 1; // Buscar en la izquierda
            }
        }

        return -1; // Elemento no encontrado
    }

    public static void main(String[] args) {
        int[] t = {8, 12, 20, 24, 28, 30, 38, 42, 50};
        int x = 12;

        int resultado = busquedaBinaria(t, x);
        if (resultado != -1) {
            System.out.println("Elemento encontrado en la posición: " + resultado);
        } else {
            System.out.println("Elemento no encontrado.");
        }
    }
}
```

---

## Salida esperada del código:

```
Elemento encontrado en la posición: 1
```

---
