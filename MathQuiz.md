# MathQuiz

## Introduction
This project is a math quiz. It is meant to quiz the user and follow some rules: 
1.   Each question gets harder after every correct answer.
2.   The program must keep track of the score and tell the user.
3.   Each question gets easier after every incorrect answer.
4.   There are four rounds total.
This project mainly uses variables, math.random, and if statements.

## Project Outline
```java
//Create scanner object and set hardness.
//Generate two random numbers
//Create score variable.
//Round 1
//Ask user to answer question.
//Check if they're answer is correct.
//If yes make next question harder.
//If no make next question easier.
//Round 2 is repeat of 1
//Round 3 is repeat of 2
//Round 4 is a repeat but here we close the game.
//Tell the user game is over.
//Tell the user their score.
```

##Source Code
```java
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
```

## Console Output
```
Hello, this is the math quiz! There are four rounds, please answer only using integers.
What is 9+3?
12
Answer Correct
Your score is: 10
What is 45+30?
75
Answer Correct
Your score is: 73
What is 187+160?
347
Answer Correct
Your score is: 286
What is 71+706?
777
Answer Correct
Game over after four rounds. Your final score is: 999
```

## Summary
For this week’s assignment we had to create a math quiz program that kept track of points and had adaptable difficulty. This proved to be difficult because of the rules of JAVA about {} brackets and how variables that are declared inside them can’t interact with other code outside of the brackets. However I eventually realized that variables declared initially in the code aren’t one-way roads and can be interacted with by statements inside the {} brackets and then affect the rest of the code. Git also proved to be invaluable in this assignment as I had to try several iterations of the code to try and figure out the best way to meet the requirements of the assignment. Because of git it was very easy to create branches and merge them back in once I was satisfied with the progress I had made.

