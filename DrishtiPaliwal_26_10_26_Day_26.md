My appraoch is to first sort arrays so that we won't miss because of taking larger one first
then traverse through arr of mug volumes and maintain sum and count variables
if sum > cup volume then break since after that all are greater volumes
else update sum and increse count;
atlast check if count >=n-1 , if true return YES else NO;

CODE:-
import java.util.Scanner;
import java.util.Arrays;
 
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
 
        int n = sc.nextInt();
        int s = sc.nextInt();
 
        int[] a = new int[n];
 
        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }
 
        Arrays.sort(a);
 
        int sum = 0;
        int count = 0;
 
        for (int i = 0; i < n; i++) {
            if (sum + a[i] > s) {
                break;
            } else {
                sum += a[i];
                count++;
            }
        }
 
        if (count >= n - 1) {
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
 
        sc.close();
    }
}

<img width="1895" height="269" alt="image" src="https://github.com/user-attachments/assets/0b5a0726-ddd7-4161-83c9-7b744f32229a" />
