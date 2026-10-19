My approach is first count no of 7 possible then check rem if rem==0 if divided by 4 the no.of 4 = rem/4
else decrease count of seven and add 7 to rem and again check
put if else inside a loop till count>= 0 
then to give min num first add 4 then add 7 to the number string
if rem !=0 after loop completes return-1;
else return num;

CODE:-

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        for (int sevens = n / 7; sevens >= 0; sevens--) {
            int rem = n - sevens * 7;

            if (rem % 4 == 0) {
                int fours = rem / 4;

                StringBuilder ans = new StringBuilder();

                for (int i = 0; i < fours; i++) {
                    ans.append('4');
                }

                for (int i = 0; i < sevens; i++) {
                    ans.append('7');
                }

                System.out.println(ans);
                sc.close();
                return;
            }
        }

        System.out.println(-1);
        sc.close();
    }
}


<img width="1890" height="178" alt="image" src="https://github.com/user-attachments/assets/dc3bb79a-9172-4d0a-aed8-2826de85078a" />
