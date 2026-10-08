import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        long sum1 = 0;

        for (int i = 0; i < n; i++) {
            sum1 += sc.nextLong();
        }

        long max = 0;
        long secMax = 0;

        for (int i = 0; i < n; i++) {
            long x = sc.nextLong();

            if (x > max) {
                secMax = max;
                max = x;
            } else if (x > secMax) {
                secMax = x;
            }
        }

        long sum2 = max + secMax;

        if (sum1 <= sum2) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }

        sc.close();
    }
}
