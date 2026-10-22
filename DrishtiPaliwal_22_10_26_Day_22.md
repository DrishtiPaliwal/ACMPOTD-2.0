
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        char[][] board = new char[n][n];

        int count = 0;

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if ((i + j) % 2 == 0) {
                    board[i][j] = 'C';
                    count++;
                } else {
                    board[i][j] = '.';
                }
            }
        }

        System.out.println(count);

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print(board[i][j]);
            }
            System.out.println();
        }

        sc.close();
    }
}

<img width="1912" height="210" alt="image" src="https://github.com/user-attachments/assets/d2192c26-4504-4795-b641-9e6fb41f0cc8" />
