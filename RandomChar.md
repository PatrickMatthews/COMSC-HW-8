#Random Capital Letter Generator

## Introduction
This project is meant to simply generate a random capital letter of the Alphabet. For this project I simply used a char variable which used a Math.random line of code, which generates a random number between 65 to 90. This range is where capital letters are.

## Outline
```java
//Declare randomLetter char variable with math.Random string inside. Limited to 65 - 90.
//Print variable to console.
```

## References and Literature

/*This is code written by Patrick Matthews that is meant to 
*generate random capital letters of the Alphabet. 
*/
public class foursixteen {
	public static void main(String[] args) {
		/*Here we generate a random number between 65 and 90
		 * We simply use a random generation line of code.
		 * We have to modify it so it only generates random captial letters.
		 * We do this by putting 65 + and *25 lines of code.
		 * And we also have to make it use char only.
		 * This limits the output to 65-90, the area for capital letters.
		 */
		char randomLetter = (char)(65 + Math.random() * 25);
		
	    //Here we simply print out the variable.
		System.out.println(randomLetter);
	}

}