import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String s1 = sc.nextLine().toLowerCase();
        String s2 = sc.nextLine().toLowerCase();

        for (int i = 0; i < s1.length(); i++) {
            int v1 = s1.charAt(i) - 'a';
            int v2 = s2.charAt(i) - 'a';

            if (v1 < v2) {
                System.out.println(-1);
                return;
            }

            if (v1 > v2) {
                System.out.println(1);
                return;
            }
        }

        System.out.println(0);
    }
}
