# RANDOM-NUMBER-GENERATOR
import java.util.Scanner;
import java.util.Random;

public class NumberGuessingGame {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int min = 1;
        int max = 100;
        int randomNumber = random.nextInt(max - min + 1) + min;
        int userGuess;

        System.out.println("Welcome to the Number Guessing Game!");
        System.out.println("I have generated a number between " + min + " and " + max + ".");
        System.out.println("Try to guess the number.");

        do {
            System.out.print("Enter your guess: ");
            userGuess = scanner.nextInt();

            if (userGuess < randomNumber) {
                System.out.println("Too low! Try again.");
            } else if (userGuess > randomNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You guessed the number.");
            }
        } while (userGuess != randomNumber);

        scanner.close();
    }
}
