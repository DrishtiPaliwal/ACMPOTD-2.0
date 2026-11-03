my approach rum while and keep subtracting the sum till i natural number from n and check if n<0 then don't increment count
at last return count

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int sum = 0;
        int i = 1;
        int count = 0;

        while (n > 0) {
            sum += i;

            if (n - sum < 0) {
                break;
            }

            n -= sum;
            count++;
            i++;
        }

        System.out.println(count);
        sc.close();
    }
}

<img width="1905" height="234" alt="image" src="https://github.com/user-attachments/assets/a9c84ba9-aa83-4c13-bd21-02c918118346" />
