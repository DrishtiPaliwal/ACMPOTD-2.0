My approach count the freq of 1,2,3 in string and then again give string as output by reaarranging them

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String s = sc.next();

        int[] freq = new int[4];

        for (int i = 0; i < s.length(); i++) {
            char ch = s.charAt(i);

            if (ch >= '1' && ch <= '3') {
                freq[ch - '0']++;
            }
        }

        StringBuilder ans = new StringBuilder();

        for (int num = 1; num <= 3; num++) {
            for (int i = 0; i < freq[num]; i++) {
                if (ans.length() > 0) {
                    ans.append('+');
                }
                ans.append(num);
            }
        }

        System.out.println(ans);
        sc.close();
    }
}

<img width="1914" height="229" alt="image" src="https://github.com/user-attachments/assets/c2471090-99cc-4cf2-badc-fc9658d511db" />
