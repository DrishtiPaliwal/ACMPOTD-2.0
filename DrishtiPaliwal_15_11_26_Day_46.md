import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int[] arr = new int[4];

        for (int i = 0; i < 4; i++) {
            arr[i] = sc.nextInt();
        }

        boolean triangle = false;
        boolean segment = false;

        for (int i = 0; i < 4; i++) {
            for (int j = i + 1; j < 4; j++) {
                for (int k = j + 1; k < 4; k++) {

                    int[] sides = {arr[i], arr[j], arr[k]};
                    Arrays.sort(sides);

                    if (sides[0] + sides[1] > sides[2]) {
                        triangle = true;
                    } else if (sides[0] + sides[1] == sides[2]) {
                        segment = true;
                    }
                }
            }
        }

        if (triangle) {
            System.out.println("TRIANGLE");
        } else if (segment) {
            System.out.println("SEGMENT");
        } else {
            System.out.println("IMPOSSIBLE");
        }

        sc.close();
    }
}

<img width="1918" height="292" alt="image" src="https://github.com/user-attachments/assets/22e1f51a-5668-4d40-acbf-07b322b60068" />
