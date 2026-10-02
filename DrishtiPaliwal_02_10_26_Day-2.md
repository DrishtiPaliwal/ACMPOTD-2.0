import java.util.*;
 
public class Main {
 
    public static void WetShark(int n, int[] arr) {
 
        long sum = 0;
 
        for (int x : arr) {
            sum += x;
        }
 
        int cnt = 0;
        ArrayList<Integer> ans = new ArrayList<>();
 
        for (int i = 0; i < n; i++) {
 
            if ((sum - arr[i]) == (long)arr[i]*(n - 1)) {
                cnt++;
                ans.add(i + 1);
            }
        }
 
        System.out.println(cnt);
 
        for (int x : ans) {
            System.out.print(x + " ");
        }
 
        System.out.println();
    }
 
    public static void main(String[] args) {
 
        Scanner sc = new Scanner(System.in);
 
        int n = sc.nextInt();
 
        int[] arr = new int[n];
 
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
 
        WetShark(n, arr);
 
        sc.close();
    }
}
