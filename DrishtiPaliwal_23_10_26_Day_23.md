My approach is to traverse through the arr and maintain secondmax and winnerindex by giving condition if arr[i] greater than max

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int max = -1;
        int secondMax = -1;
        int winnerIndex = -1;

        for (int i = 0; i < n; i++) {
            if (arr[i] > max) {
                secondMax = max;
                max = arr[i];
                winnerIndex = i + 1;
            } else if (arr[i] > secondMax) {
                secondMax = arr[i];
            }
        }

        System.out.println(winnerIndex + " " + secondMax);

        sc.close();
    }
}

<img width="1876" height="225" alt="image" src="https://github.com/user-attachments/assets/96fc74dc-23f7-49e2-a058-34303b1b1890" />
