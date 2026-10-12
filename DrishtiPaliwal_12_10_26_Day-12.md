import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String s = sc.next();
        int count = 0;

        for (int i = 0; i < s.length(); i++) {
            if (Character.isLowerCase(s.charAt(i))) {
                count++;
            }
        }

        if (count >= s.length() - count) {
            System.out.println(s.toLowerCase());
        } else {
            System.out.println(s.toUpperCase());
        }

        sc.close();
    }
}
