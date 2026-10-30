My approach is to make freq arr to store count of characters of heading after taking input
then make a boolean variable possible to cheack whether the charcter of text exists in heading if possible false break the loop
atlast return YES or NO according to possible boolean

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String heading = sc.nextLine();
        String text = sc.nextLine();

        int[] freq = new int[256];

        // Count characters in the heading, ignoring spaces
        for (int i = 0; i < heading.length(); i++) {
            char c = heading.charAt(i);
            if (c != ' ') {
                freq[c]++;
            }
        }

        boolean possible = true;

        // Check whether the text can be formed
        for (int i = 0; i < text.length(); i++) {
            char c = text.charAt(i);

            if (c == ' ') {
                continue;
            }

            if (freq[c] == 0) {
                possible = false;
                break;
            }

            freq[c]--;
        }

        System.out.println(possible ? "YES" : "NO");

        sc.close();
    }
}

<img width="1860" height="243" alt="image" src="https://github.com/user-attachments/assets/ce25a7b1-d64e-4873-96dd-b5d9cae557df" />
