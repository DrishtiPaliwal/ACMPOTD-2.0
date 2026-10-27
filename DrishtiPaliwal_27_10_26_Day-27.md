My approach is that first make char array by taking string input and then short them 
then make a string using for loop from 1 to n , then 
for trailing zeroes use first while loop to identify index of ele just after 0 
then swaping first index zero with the index identified 
then check whether it is equal to bob answer if yes then"OK" else "WRONG_ANSWER"

CODE:-
import java.util.*;
 
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
 
        String n = sc.next();
        String m = sc.next();
 
        char[] arr = n.toCharArray();
        Arrays.sort(arr);
 
        StringBuilder num = new StringBuilder();
 
        for (int i = 0; i < arr.length; i++) {
            num.append(arr[i]);
        }
 
        int i = 0;
 
        while (i < num.length() && num.charAt(i) == '0') {
            i++;
        }
 
        if (i < num.length()) {
            char temp = num.charAt(0);
            num.setCharAt(0, num.charAt(i));
            num.setCharAt(i, temp);
        }
 
        if (num.toString().equals(m)) {
            System.out.println("OK");
        } else {
            System.out.println("WRONG_ANSWER");
        }
 
        sc.close();
    }
}

<img width="1891" height="269" alt="image" src="https://github.com/user-attachments/assets/05f873b1-e494-4fde-957b-f817cca27e28" />
