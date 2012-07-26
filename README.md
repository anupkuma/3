3
=

Design an algorithm and write code to remove the duplicate characters in a string without using any additional buffer. NOTE: One or two additional variables are fine. An extra copy of the array is not.



Just like first question, we have created a Boolean array and set the value to True in array for each character that we find while scanning through the String. But while checking the repetition inside IF condition, we have used ‘Continue’ so that loop again starts from beginning else adding the value to the variable newStr. Then finally printing the newStr.
import java.util.Scanner;

public class NoDuplication {
  public static void main(String[] args) {

		boolean[] char_set = new boolean[256];
		
		Scanner in = new Scanner(System.in);
		System.out.println("Enter a string");
		String str = in.nextLine();
		System.out.println("You enterd " + str);
		String newStr=" ";
		
		
		for (int i = 0; i < str.length(); i++) {
			int val = str.charAt(i);
			
			if (char_set[val]) {
				
				continue;
			}
			char_set[val] = true;
			newStr = newStr + str.charAt(i); 
		}
		System.out.println("String without duplicate is " + newStr);
	}
}
