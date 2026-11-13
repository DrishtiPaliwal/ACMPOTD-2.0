My approach is maintaining sum of left and right side of cut and then checking at each cut whether it is same or not
if same then increment a count variable and cut will one less than length of arr
atlast return count

CODE:-
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        int total = 0;

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            total += arr[i];
        }

        int left = 0;
        int right = total;
        int count = 0;

        for (int i = 0; i < n - 1; i++) {
            left += arr[i];
            right -= arr[i];

            if (left == right) {
                count++;
            }
        }

        System.out.println(count);

        sc.close();
    }
}


<img width="1904" height="322" alt="image" src="https://github.com/user-attachments/assets/6b84c622-389a-45fa-b003-cccb7bc22447" />
