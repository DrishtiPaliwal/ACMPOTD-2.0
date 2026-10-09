import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int sum = 0;

        for (int i = 1; sum < n; i++) {
            sum += i;

            if (sum == n) {
                System.out.println("YES");
                sc.close();
                return;
            }
        }

        System.out.println("NO");
        sc.close();
    }
}
