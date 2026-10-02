import java.util.*;

public class Main {

    public static long WetShark(int n, int[] arr) {
        long sum = 0;
        int min_odd = Integer.MAX_VALUE;

        for (int i = 0; i < n; i++) {
            sum += arr[i];

            if (arr[i] % 2 == 1) {
                min_odd = Math.min(min_odd, arr[i]);
            }
        }

        if (sum % 2 == 1) {
            sum -= min_odd;
        }

        return sum;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.println(WetShark(n, arr));

        sc.close();
    }
}
