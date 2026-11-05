My approach is traversing the loop till w and adding i*k to sum variable everytime
atlast return max(0,sum-n)

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int k = sc.nextInt();
        int n = sc.nextInt();
        int w = sc.nextInt();

        int sum = 0;

        for (int i = 1; i <= w; i++) {
            sum += k * i;
        }

        System.out.println(Math.max(0, sum - n));

        sc.close();
    }
}

<img width="1848" height="220" alt="image" src="https://github.com/user-attachments/assets/0b60da43-a685-4907-8d1d-e0b4b94cee9a" />
