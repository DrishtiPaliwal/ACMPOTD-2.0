My approach is running a while loop till x%k!=0 and increment x by 1 everytime
atlast when loop ends return x

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        long n = sc.nextLong();
        long k = sc.nextLong();

        long x = n + 1;

        while (x % k != 0) {
            x++;
        }

        System.out.println(x);

        sc.close();
    }
}

<img width="1869" height="313" alt="image" src="https://github.com/user-attachments/assets/eadb1e89-aa5a-4dc2-8627-811befeeff16" />
