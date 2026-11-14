My approach traverse through string and store count of anton and dainik respectively.
after that check the condition and get the desired output

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        String s = sc.next();

        int a = 0;
        int d = 0;

        for (int i = 0; i < n; i++) {
            if (s.charAt(i) == 'A') {
                a++;
            } else {
                d++;
            }
        }

        if (a > d) {
            System.out.println("Anton");
        } else if (d > a) {
            System.out.println("Danik");
        } else {
            System.out.println("Friendship");
        }

        sc.close();
    }
}
<img width="1916" height="325" alt="image" src="https://github.com/user-attachments/assets/f20209ec-f44d-4078-8ea7-421ab8cb1196" />
