import java.util.*;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int minDiff = Integer.MAX_VALUE;
        int ans1 = 0;
        int ans2 = 1;

        for (int i = 0; i < n; i++) {

            int next = (i + 1) % n;

            int diff = Math.abs(arr[i] - arr[next]);

            if (diff < minDiff) {
                minDiff = diff;
                ans1 = i;
                ans2 = next;
            }
        }

        System.out.println((ans1 + 1) + " " + (ans2 + 1));

        sc.close();
    }
}
