My approach by storing storing in hashset, can get the number of distinct pair he have.
Then by subtracting hashset size from 4 we get the answer for how many minimum no. of horseshoes he need to buy.

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int[] arr = new int[4];

        for (int i = 0; i < 4; i++) {
            arr[i] = sc.nextInt();
        }

        HashSet<Integer> set = new HashSet<>();

        for (int i = 0; i < 4; i++) {
            set.add(arr[i]);
        }

        System.out.println(4 - set.size());

        sc.close();
    }
}

<img width="1813" height="133" alt="image" src="https://github.com/user-attachments/assets/2c7d4947-5a46-416b-9b01-0d0837d706bd" />
