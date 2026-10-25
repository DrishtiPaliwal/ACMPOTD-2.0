My approach is to first traversing through first integers array and give them their choice apples
then after checking the availabilty of second person choice from ans array giving them their choice apples
then atlast return ans;

CODE:-
import java.util.*;
 
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
 
        int n = sc.nextInt();
        int a = sc.nextInt();
        int b = sc.nextInt();
 
        int[] ans = new int[n];
 
        for (int i = 0; i < a; i++) {
            int apple = sc.nextInt();
            ans[apple - 1] = 1;
        }
 
        for (int i = 0; i < b; i++) {
            int apple = sc.nextInt();
 
            if (ans[apple - 1] != 1) {
                ans[apple - 1] = 2;
            }
        }
 
        for (int i = 0; i < n; i++) {
            System.out.print(ans[i] + " ");
        }
 
        System.out.println();
        sc.close();
    }
}

<img width="1893" height="339" alt="image" src="https://github.com/user-attachments/assets/f1a41bdc-e184-4429-b460-7166196c1820" />
