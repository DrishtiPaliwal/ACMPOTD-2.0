import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int prev = sc.nextInt();
        int count = 1;
        int maxLength = 1;

        for (int i = 1; i < n; i++) {
            int curr = sc.nextInt();

            if (curr > prev) {
                count++;
            } else {
                count = 1;
            }

            maxLength = Math.max(maxLength, count);
            prev = curr;
        }

        System.out.println(maxLength);

        sc.close();
    }
}

<img width="1893" height="311" alt="image" src="https://github.com/user-attachments/assets/2128bca5-0de9-4dff-a506-2c75fda5c4fd" />
