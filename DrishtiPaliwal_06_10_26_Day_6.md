import java.util.*;

public class Main {

    public static boolean isPalindrome(int n) {
        int original = n;
        int reverse = 0;

        while (n > 0) {
            int rem = n % 10;
            reverse = reverse * 10 + rem;
            n /= 10;
        }

        return original == reverse;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int x = sc.nextInt();

        // Remove trailing zeroes
        while (x % 10 == 0) {
            x /= 10;
        }

        if (isPalindrome(x)) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }

        sc.close();
    }
}
