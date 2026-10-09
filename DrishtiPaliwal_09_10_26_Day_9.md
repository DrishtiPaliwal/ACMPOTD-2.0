import java.util.*;
 
public class Main {
 
    public static long TheatreSquare(int n, int m, int a) {
        long l = ((long)n + a - 1) / a;
        long b = ((long)m + a - 1) / a;
        long ans = l * b;
        return ans;
    }
 
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
 
        int n = sc.nextInt();
        int m = sc.nextInt();
        int a = sc.nextInt();
 
        System.out.println(TheatreSquare(n, m, a));
 
        sc.close();
    }
}
