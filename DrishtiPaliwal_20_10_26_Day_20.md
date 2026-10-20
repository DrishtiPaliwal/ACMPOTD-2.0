My approach uppercase the first character of string and then adding the remaining string to final ans

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String s = sc.next();

        s = Character.toUpperCase(s.charAt(0)) + s.substring(1);

        System.out.println(s);

        sc.close();
    }
}

<img width="1877" height="229" alt="image" src="https://github.com/user-attachments/assets/0d5f9dbc-5a3a-4738-bdd1-17251f21c0e7" />
