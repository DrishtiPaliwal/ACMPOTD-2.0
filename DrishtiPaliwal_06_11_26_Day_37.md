My approach is to check if (a<b) then arr[0] = a and give arr[1] = (b-a)/2;
else arr[0] = b and give arr[1] = (a-b)/2;
return arr

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        int[] arr = new int[2];

        if (a < b) {
            arr[0] = a;
            int rem = b - a;
            arr[1] = rem / 2;
        } else {
            arr[0] = b;
            int rem = a - b;
            arr[1] = rem / 2;
        }

        System.out.println(arr[0] + " " + arr[1]);

        sc.close();
    }
}

<img width="1905" height="215" alt="image" src="https://github.com/user-attachments/assets/89346bc7-dbc8-42c4-91f8-a10a9b3b8969" />
