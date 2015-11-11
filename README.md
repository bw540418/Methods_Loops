# Methods and Loops HW9
This is my project description

## Java Code
```java
import java.util.Scanner;

public class Loops_Methods {

	public static void main(String[] args) {
		System.out.println("Hello Class.");
		
		//call the addition game method
		additionGameMethod();
	}
				public static void additionGameMethod() {
						//debugging statement
						System.out.println("Inside the addition game method.");
	
							int hardness = 5;
							int hardnessStep = 2;
							int score = 0;
	
							// set up loop to go through the number of rounds
							int numberOfRounds = 3;
							for(int roundNumber = 1;
							roundNumber <= numberOfRounds;
							roundNumber = roundNumber +1){
								System.out.println("inside the for loop. Round: " + roundNumber);
								boolean isAnswerCorrect = getAndCheckStudentAnswer(hardness);
								if(isAnswerCorrect){
									System.out.print("Your score was " + score + " and is now ");
									score = score + hardness;
									System.out.println(score + ".");
								}else{
									if(roundNumber<numberOfRounds){
										System.out.print("Your hardness was " + hardness + " and is now ");
										if(hardness>5){
											hardness = hardness / hardnessStep;
											
										}
										System.out.println(hardness + ".");
									}
								}
							}
							
							
									
							System.out.println("The game is complete.");
							System.out.println("Your final score was " + score );
				}

							
						
						
	public static boolean getAndCheckStudentAnswer(int hardness) {
	System.out.println("inside get and check student answer method");
	int number1 = (int)(Math.random()*hardness);
	int number2 = (int)(Math.random()*hardness);
	System.out.println("add " + number1 + " and " + number2 + ".");
	//Scanner input = new Scanner(System.in);
	//int studentAnswer = input.nextInt();
	Scanner get = new Scanner(System.in);
	int studentAnswer = get.nextInt();
	if(studentAnswer == (number1 + number2)){
		System.out.println("Good work, your answer was correct.");
		return true;
	}else{
		System.out.println("Nice try, but the correct answer was " + (number1 + number2));
		return false;
		}
	
	}	
	
}

```

## Console Output
```
Hello Class.
Inside the addition game method.
inside the for loop. Round: 1
inside get and check student answer method
add 2 and 0.
2
Good work, your answer was correct.
Your score was 0 and is now 5.
inside the for loop. Round: 2
inside get and check student answer method
add 2 and 2.
4
Good work, your answer was correct.
Your score was 5 and is now 10.
inside the for loop. Round: 3
inside get and check student answer method
add 1 and 0.
1
Good work, your answer was correct.
Your score was 10 and is now 15.
The game is complete.
Your final score was 15
```

## Command Prompt Output
```
this is where we put the command from cmd 
```

## References


## Conclusion
This was an example of Markdown documentation as we have done in the past.
