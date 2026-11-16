
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                for (int k = j + 1; k < n; k++) {

                    if (i != j && i != k &&
                        arr[i] == arr[j] + arr[k]) {

                        System.out.println((i + 1) + " " +
                                           (j + 1) + " " +
                                           (k + 1));
                        return;
                    }
                }
            }
        }

        System.out.println(-1);
        sc.close();
    }
}
<img width="1918" height="245" alt="image" src="https://github.com/user-attachments/assets/a040a78f-649b-4dc9-b16f-35869778ac9b" />
