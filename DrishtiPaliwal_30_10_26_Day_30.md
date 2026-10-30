My approach is to first make int count variable after taking input then
run for loop for iterating in rows till n then use if condition (arr[i][1]-arr[i][0]>=2)
increment count if true and return count atlast;

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int[][] arr = new int[n][2];

        for (int i = 0; i < n; i++) {
            arr[i][0] = sc.nextInt();
            arr[i][1] = sc.nextInt();
        }

        int count = 0;

        for (int i = 0; i < n; i++) {
            if (arr[i][1] - arr[i][0] >= 2) {
                count++;
            }
        }

        System.out.println(count);

        sc.close();
    }
}

<img width="1909" height="379" alt="image" src="https://github.com/user-attachments/assets/51f79654-1abf-4e4e-878b-94214c0ea5d7" />
