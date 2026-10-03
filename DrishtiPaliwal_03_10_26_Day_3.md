import java.util.*;

public class Main {

    public static String TheTime(String time, int mins) {
        String[] parts = time.split(":");
        int hour = Integer.parseInt(parts[0]);
        int minute = Integer.parseInt(parts[1]);
        
        int hr = (minute +mins)/60;
        minute = (minute +mins)%60;
        hour = (hour+hr)%24;
        
        
        return String.format("%02d:%02d", hour, minute);
        
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        String s = sc.next();
        int n = sc.nextInt();

        System.out.println(TheTime(s, n));

        sc.close();
    }
}
