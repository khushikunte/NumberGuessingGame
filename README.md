# NumberGuessingGame
import java.util.Random;
import java.util.Scanner;

public class NumberGuessingGame {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);//to take user Input
		String play="yes";
		while(play.equals("yes")) {       //if you are going to play the game again
			Random random=new Random();
			int randnum=random.nextInt(100);
			int guess=-1;
			int tries=0;
		while(guess!=randnum) {           //check if the game is over
			System.out.println("Guess a num between 1 and 100!");
			guess=sc.nextInt();
			tries++;
		if(guess==randnum) {              //check whether the number is been guessed or not!
			System.out.println("==================================");
			System.out.println("Awesome! You guessed the number!");
			System.out.println("It only took you\t"+tries+"\tGuesses!");
			System.out.println("==================================");
			System.out.println("Would you like to play again?Yes or No:");
			play=sc.next().toLowerCase();
			
		}
		else if(guess>randnum) {
			System.out.println("Your guess is to high, Try Again!");
		}
		else {
			System.out.println("Your guess is too Low, Try Again!");
		}
		}
		}

	}

}
