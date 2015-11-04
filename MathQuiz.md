/* This is a math quiz program written by Patrick Matthews
 * This game has some rules:
 * 1. Each question gets harder after every correct answer.
 * 2. The program must keep track of the score and tell the user.
 * 3. Each question gets easier after every incorrect answer.
 * 4. There are four rounds total.
 */
import java.util.Scanner;
public class MathQuiz {
public static void main(String[] args) {
	
				//Create scannner object and initial hardness.
	            Scanner input     = new Scanner(System.in);
				int hardness      = 10;
				//Generate two numbers for the first problem.
				int number1       = (int)(Math.random() * hardness);
				int number2       = (int)(Math.random() * hardness);
				//We create a variable for score we can add onto.		
				int score         = 0;
				//We also make variables for their answers, to simplify code later on.
				int correctAnswer = number1 + number2;
				
				// Round 1
				// Ask the user to add these two numbers together
				System.out.println("Hello, this is the math quiz! "
						+ "There are four rounds, please answer only using integers.");
			
				System.out.println("What is " + number1 + "+" + number2 + "?" );
				//Get their response.
				int studentanswer = input.nextInt();
				//Check if the answer was correct
				if(studentanswer  == correctAnswer){	
				   //if correct tell them its correct
				   System.out.println("Answer Correct");
				   //Give them points
				   score    += hardness;
				   //Tell them their score
				   System.out.println("Your score is: "
						+ score);
				   //Make the next question harder
				   hardness += 53;
				//If wrong, tell them and lower difficulty of next question.
				}else if(studentanswer!= correctAnswer){
					System.out.println("Sorry, that's incorrect.");
					hardness *=2;
				}
				
				
				//Round Two
				//Now we need to make two new numbers for the next round.
				int number3 = (int)(Math.random() * hardness);
				int number4 = (int)(Math.random() * hardness);
				// We ask them again but the numbers will be harder now.
				System.out.println("What is " + number3 + "+" + number4 + "?" );
				//Get their response.
				int studentanswertwo = input.nextInt();
				int correctAnswertwo = number3 + number4;
				//Check if the answer was correct
				if(studentanswertwo  == correctAnswertwo){
				   /*if correct, tell them its correct,then raise their score,
					*increase the difficulty of the next question, and tell them their score.
					*/
				   System.out.println("Answer Correct");
			       score    += hardness;
			       hardness += 150;
			       System.out.println("Your score is: "
						+ score);
			    //if incorrect tell them and make the next question easier.
				}else if(studentanswertwo!= correctAnswertwo){
					System.out.println("Sorry, that's incorrect.");
					hardness +=50;
				}
				
				//Round Three
				//Now we need to make two new numbers for the next round.
				int number5 = (int)(Math.random() * hardness);
				int number6 = (int)(Math.random() * hardness);
				// We ask them again but the numbers will be harder now.
				System.out.println("What is " + number5 + "+" + number6 + "?" );
				//Get their response.
				int studentanswerthree = input.nextInt();
				int correctAnswerthree = number5 + number6;
				//Check if the answer was correct
				if(studentanswerthree  == correctAnswerthree){
			       /*if correct, tell them its correct,then raise their score,
				    *increase the difficulty of the next question, and tell them their score.
				    */
				   System.out.println("Answer Correct");
			       score    += hardness;
			       hardness += 500;
			       System.out.println("Your score is: "
						+ score);
				}else if(studentanswerthree!= correctAnswerthree){
					System.out.println("Sorry, that's incorrect.");
					hardness +=120;
				}
				
				//Round Four
				//Now we need to make two new numbers for the next round.
				int number7 = (int)(Math.random() * hardness);
				int number8 = (int)(Math.random() * hardness);
				// We ask them again but the numbers will be harder now.
				System.out.println("What is " + number7 + "+" + number8 + "?" );
				//Get their response.
				int studentanswerfour = input.nextInt();
				int correctAnswerfour = number7 + number8;
				//Check if the answer was correct
				if(studentanswerfour  == correctAnswerfour){
				   //if correct, tell them its correct, and raise their score,
				   System.out.println("Answer Correct");
			       score    += hardness;
			    //If incorrect, tell them.
				}else if(studentanswerfour!= correctAnswerfour){
				   System.out.println("Sorry, that's incorrect.");
				}
				   //The game is over after four rounds and we tell them their score.
				   System.out.println("Game over after four rounds. Your final score is: "
						+ score);
		}

}