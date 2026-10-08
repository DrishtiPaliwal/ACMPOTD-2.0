import java.util.*;
 
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
 
        String s = sc.next();
        String t = sc.next();
 
        if (s.length() != t.length()) {
            System.out.println("NO");
            return;
        }
 
        int i = 0;
        int j = t.length() - 1;
 
        while (i < s.length() && j >= 0) {
            if (s.charAt(i) != t.charAt(j)) {
                System.out.println("NO");
                return;
            }
 
            i++;
            j--;
        }
 
        System.out.println("YES");
 
        sc.close();
    }
}
