My approach is first check whether it divisible by k or not , if not then return -1;
next make freq arr to count freq of letters and then check if freq is divisible by k, if freq not divisible by k then return -1;
and also while checking freq run nested loop and add letters to stringbuilder 
ans then make one more string and add previous stringbuilder k times using for loop

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int k = sc.nextInt();
        String s = sc.next();

        if (s.length() % k != 0) {
            System.out.println(-1);
            return;
        }

        int[] freq = new int[26];

        for (int i = 0; i < s.length(); i++) {
            freq[s.charAt(i) - 'a']++;
        }

        StringBuilder part = new StringBuilder();

        for (int i = 0; i < 26; i++) {
            if (freq[i] % k != 0) {
                System.out.println(-1);
                return;
            }

            for (int j = 0; j < freq[i] / k; j++) {
                part.append((char) ('a' + i));
            }
        }

        StringBuilder ans = new StringBuilder();

        for (int i = 0; i < k; i++) {
            ans.append(part);
        }

        System.out.println(ans);
        sc.close();
    }
}

<img width="1918" height="241" alt="image" src="https://github.com/user-attachments/assets/0a066df5-eec8-47f0-a60e-a986508d78b2" />
