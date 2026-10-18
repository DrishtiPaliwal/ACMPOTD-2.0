My approach for this question is checking whether two consecutive characters in a string are same or not.
If they are same ,then increase the count for mininum no. of characters to be taken out to sastify the situation

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        String s = sc.next();

        int count = 0;

        for (int i = 1; i < n; i++) {
            if (s.charAt(i - 1) == s.charAt(i)) {
                count++;
            }
        }

        System.out.println(count);

        sc.close();
    }
}

<img width="1898" height="196" alt="image" src="https://github.com/user-attachments/assets/6226317a-5f19-444b-aa19-29bc7d4eca83" />
