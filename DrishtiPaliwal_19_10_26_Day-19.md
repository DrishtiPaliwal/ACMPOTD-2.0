My approach incrementing the year till we won't get the year which is greater than given year and minimum year which have all four distinct digits.
after that run loop from 1->n-1 and run for loop inside from i+1 to n and check if charat(i) == charat(j)
If true then increment year else return that year.

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int y = sc.nextInt();
        y++;

        while (true) {
            String s = String.valueOf(y);
            boolean distinct = true;

            for (int i = 0; i < s.length(); i++) {
                for (int j = i + 1; j < s.length(); j++) {
                    if (s.charAt(i) == s.charAt(j)) {
                        distinct = false;
                        break;
                    }
                }

                if (!distinct) {
                    break;
                }
            }

            if (distinct) {
                System.out.println(y);
                break;
            }

            y++;
        }

        sc.close();
    }
}

<img width="1851" height="210" alt="image" src="https://github.com/user-attachments/assets/9eb88c9f-5e46-4e36-911b-603ba922a20b" />
