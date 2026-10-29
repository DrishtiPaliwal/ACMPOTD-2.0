import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        int mid = n / 2;

        for (int i = 0; i < n; i++) {
            int stars;

            if (i <= mid) {
                stars = mid - i;
            } else {
                stars = i - mid;
            }

            for (int j = 0; j < stars; j++) {
                System.out.print("*");
            }

            for (int j = 0; j < n - 2 * stars; j++) {
                System.out.print("D");
            }

            for (int j = 0; j < stars; j++) {
                System.out.print("*");
            }

            System.out.println();
        }

        sc.close();
    }
}

<img width="1907" height="227" alt="image" src="https://github.com/user-attachments/assets/a23f20f3-2c11-455b-a889-4d3af9c988b2" />
