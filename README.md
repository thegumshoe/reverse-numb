# reverse-numb
Application to reverse an inputted number.

import java.util.Scanner;

public class ReverseNum {
	private static Scanner s;

	public static void main(String[] args){
		//Variable declaration 
		int input;
		int result = 0;
		int remainder;
		s = new Scanner(System.in);
		System.out.println("Please enter a numeric number:");
		//User input int values
		input = s.nextInt();
		while(input > 0){
			//Get the current remainder of the user input value. 
			remainder  = input % 10;
			//Removes the current remainder from the inputted value
			input = input / 10;
			//Appends the new remainder to the previous reminder, in turn causing a reverse order. 
			result = result * 10 + remainder;
		}
		//Display reversed input
		System.out.println("The reversed number is: " + result);
	}
}
