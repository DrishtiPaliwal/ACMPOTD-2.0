My approach is using bit manipulation since
a^a = 0  ;  0^a = a;
there taking xor for all numbers from 1 to n and for all elements in arr sepearately
then taking their xor will cancel out same and only missing one will be left

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int xor1 = 0;
        int xor2 = 0;

        for (int i = 1; i <= n; i++) {
            xor1 ^= i;
        }

        for (int i = 0; i < n - 1; i++) {
            int x = sc.nextInt();
            xor2 ^= x;
        }

        System.out.println(xor1 ^ xor2);

        sc.close();
    }
}

<img width="1912" height="215" alt="image" src="https://github.com/user-attachments/assets/42d1fd9a-5a24-43e9-adf6-bd147f1dbc18" />
