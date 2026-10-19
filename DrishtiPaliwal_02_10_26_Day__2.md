import java.util.*;

public class Main {

    public static String Flag(int n, int m, char[][] mat) {

        for (int i = 0; i < n - 1; i++) {
            if (mat[i][0] == mat[i + 1][0]) {
                return "NO";
            }
        }

        for (int i = 0; i < n; i++) {
            char val = mat[i][0];

            for (int j = 1; j < m; j++) {
                if (mat[i][j] != val) {
                    return "NO";
                }
            }
        }

        return "YES";
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int m = sc.nextInt();

        char[][] mat = new char[n][m];

        // Take row-wise input
        for (int i = 0; i < n; i++) {
            mat[i] = sc.next().toCharArray();
        }

        // Call Flag
        System.out.println(Flag(n, m, mat));

        sc.close();
    }
}
