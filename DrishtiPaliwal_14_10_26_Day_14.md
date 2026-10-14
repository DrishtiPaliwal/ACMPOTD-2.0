import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        HashMap<Integer, Integer> map = new HashMap<>();

        for (int i = 0; i < n; i++) {
            map.put(arr[i], map.getOrDefault(arr[i], 0) + 1);
        }

        int maxFreq = 0;

        for (int freq : map.values()) {
            maxFreq = Math.max(maxFreq, freq);
        }

        System.out.println(maxFreq + " " + map.size());

        sc.close();
    }
}
