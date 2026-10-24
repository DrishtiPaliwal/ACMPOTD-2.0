My approach is first checking the required length , if less than required length return too weak;
next traverse through string and make boolean variables for each since we need atleast one , 
so if booalean for any of them is false then return too weak
and then atlast return correct

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String s = sc.next();

        if (s.length() < 5) {
            System.out.println("Too weak");
            return;
        }

        boolean lower = false;
        boolean upper = false;
        boolean digit = false;

        for (int i = 0; i < s.length(); i++) {
            char ch = s.charAt(i);

            if (ch >= 'a' && ch <= 'z') {
                lower = true;
            } else if (ch >= 'A' && ch <= 'Z') {
                upper = true;
            } else if (ch >= '0' && ch <= '9') {
                digit = true;
            }
        }

        if (!lower || !upper || !digit) {
            System.out.println("Too weak");
        } else {
            System.out.println("Correct");
        }

        sc.close();
    }
}


<img width="1912" height="229" alt="image" src="https://github.com/user-attachments/assets/ba293f34-e577-4b07-8f86-b88448a17add" />
