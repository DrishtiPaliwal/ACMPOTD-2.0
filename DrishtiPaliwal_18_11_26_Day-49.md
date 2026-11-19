
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int count = 0;

        for (int i = 2; i <= n; i++) {
            int num = i;
            int primeCount = 0;

            for (int j = 2; j <= num; j++) {
                if (num % j == 0) {
                    primeCount++;

                    while (num % j == 0) {
                        num /= j;
                    }
                }
            }

            if (primeCount == 2) {
                count++;
            }
        }

        System.out.println(count);
        sc.close();
    }
}

<img width="1911" height="239" alt="image" src="https://github.com/user-attachments/assets/ea6d514f-6330-4796-9db5-602786fb131c" />
