import java.util.*;
 
public class Main {
 
    public static String SecondOrderStats(int n, int[] arr) {
        int min = Integer.MAX_VALUE;
        int secmin = Integer.MAX_VALUE;
 
        if (n == 1) {
            return "NO";
        }
 
        for (int i = 0; i < n; i++) {
            if (arr[i] < min) {
                secmin = min;
                min = arr[i];
            } 
            else if (arr[i] > min && arr[i] < secmin) {
                secmin = arr[i];
            }
        }
 
        if (secmin == Integer.MAX_VALUE) {
            return "NO";
        }
 
        return String.valueOf(secmin);
    }
 
    public static void main(String[] args) {
 
        Scanner sc = new Scanner(System.in);
 
        int n = sc.nextInt();
 
        int[] arr = new int[n];
 
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
 
        System.out.println(SecondOrderStats(n, arr));
 
        sc.close();
    }
}
