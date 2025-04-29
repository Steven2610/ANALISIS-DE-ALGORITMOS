# Tarea semana 2

![4cb24fbe-5149-4378-bff4-d055493e2c53](https://github.com/user-attachments/assets/7ca7439f-52ba-4920-9cd8-6f7b53a1e5d0)

resolucion de ejerccicios 


![WhatsApp Image 2025-04-29 at 12 07 35 PM](https://github.com/user-attachments/assets/43028b0d-88a7-4c57-aeeb-6e1e550ee49a)


```java
public class MergeSort {

    public static void merge(int[] A, int p, int q, int r) {
        int nL = q - p + 1; // length of A[p..q]
        int nR = r - q;     // length of A[q+1..r]

        // Create temporary arrays
        int[] L = new int[nL];
        int[] R = new int[nR];

        // Copy data to temporary arrays
        for (int i = 0; i < nL; i++) {
            L[i] = A[p + i];
        }

        for (int j = 0; j < nR; j++) {
            R[j] = A[q + 1 + j];
        }

        // Merge the temporary arrays back into A[p..r]
        int i = 0, j = 0;
        int k = p;

        while (i < nL && j < nR) {
            if (L[i] <= R[j]) {
                A[k] = L[i];
                i++;
            } else {
                A[k] = R[j];
                j++;
            }
            k++;
        }

        // Copy any remaining elements of L[]
        while (i < nL) {
            A[k] = L[i];
            i++;
            k++;
        }

        // Copy any remaining elements of R[]
        while (j < nR) {
            A[k] = R[j];
            j++;
            k++;
        }
    }
}
```
