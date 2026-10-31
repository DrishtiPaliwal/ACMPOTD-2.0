My approach is traking elements by using boolean arr of length n
first traverse through first given array and mark the level true
then while traversing through next first check whteher it is marked if true then continue else mark
atlast traverse boolean arr and check for any false value if found any false then return oh my keyboard 
else return I am a guy

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        boolean[] arr = new boolean[n];

        int p = sc.nextInt();

        for (int i = 0; i < p; i++) {
            int level = sc.nextInt();
            arr[level - 1] = true;
        }

        int q = sc.nextInt();

        for (int i = 0; i < q; i++) {
            int level = sc.nextInt();
            arr[level - 1] = true;
        }

        boolean possible = true;

        for (int i = 0; i < n; i++) {
            if (!arr[i]) {
                possible = false;
                break;
            }
        }

        System.out.println(possible ? "I become the guy." : "Oh, my keyboard!");

        sc.close();
    }
}

<img width="1898" height="224" alt="image" src="https://github.com/user-attachments/assets/32c35910-5436-405e-ab46-12c42c326696" />
