My approach is to store the matchbox and no. of matches in 2D array and then
sorting the arr wrt no. of matches 
then using for loop maintain the sum of matches within required 
atlast return sum

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int m = sc.nextInt();

        int[][] arr = new int[m][2];

        for (int i = 0; i < m; i++) {
            arr[i][0] = sc.nextInt(); // Number of matchboxes
            arr[i][1] = sc.nextInt(); // Matches per matchbox
        }

        Arrays.sort(arr, (a, b) -> Integer.compare(b[1], a[1]));

        long total = 0;

        for (int i = 0; i < m && n > 0; i++) {
            int take = Math.min(n, arr[i][0]);

            total += (long) take * arr[i][1];
            n -= take;
        }

        System.out.println(total);
        sc.close();
    }
}

<img width="1900" height="232" alt="image" src="https://github.com/user-attachments/assets/f8403b0a-4868-4319-9316-c4064116083c" />
