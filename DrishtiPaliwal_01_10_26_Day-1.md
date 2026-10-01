import java.util.*;

public class Main {

    public static char[][] letter(int n, int m, char[][] mat) {
        int min_r = n;
        int max_r = -1;
        int min_c = m;
        int max_c = -1;

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                if (mat[i][j] == '*') {
                    min_r = Math.min(min_r, i);
                    max_r = Math.max(max_r, i);
                    min_c = Math.min(min_c, j);
                    max_c = Math.max(max_c, j);
                }
            }
        }

        int row = max_r - min_r + 1;
        int col = max_c - min_c + 1;

        char[][] ans = new char[row][col];

        int a = 0;
        int b = 0;

        for (int i = min_r; i <= max_r; i++) {
            b = 0;
            for (int j = min_c; j <= max_c; j++) {
                ans[a][b] = mat[i][j];
                b++;
            }
            a++;
        }

        return ans;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int m = sc.nextInt();

        char[][] mat = new char[n][m];

        for (int i = 0; i < n; i++) {
            mat[i] = sc.next().toCharArray();
        }

        char[][] ans = letter(n, m, mat);

        for (int i = 0; i < ans.length; i++) {
            for (int j = 0; j < ans[0].length; j++) {
                System.out.print(ans[i][j]);
            }
            System.out.println();
        }

        sc.close();
    }
}
