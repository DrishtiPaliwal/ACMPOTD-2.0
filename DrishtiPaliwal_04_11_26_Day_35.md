My approach is to first lowercase the string and then make boolean arr of 26
then we iterate over string and mark freq true also check if already mark true then continue
atlast iterate over boolean freq and check if any is false return NO else return YES

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        String s = sc.next().toLowerCase();

        boolean[] freq = new boolean[26];

        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            freq[c - 'a'] = true;
        }

        boolean pangram = true;

        for (int i = 0; i < 26; i++) {
            if (!freq[i]) {
                pangram = false;
                break;
            }
        }

        System.out.println(pangram ? "YES" : "NO");

        sc.close();
    }
}

<img width="1905" height="243" alt="image" src="https://github.com/user-attachments/assets/d5c3a932-846c-472b-924b-65090c34d8b3" />
