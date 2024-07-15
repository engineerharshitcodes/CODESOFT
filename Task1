import java.util.Random;
import java.util.Scanner;

    public class GuessTheNumberGame {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            Random random = new Random();
            int totalScore = 0;
            int rounds = 0;
            boolean playAgain = true;

            System.out.println("The guess game welcomes you!");

            while (playAgain) {
                rounds++;
                int numberToGuess = random.nextInt(100) + 1;
                int attempts = 0;
                boolean GuessedCorrectly = false;

                System.out.println("\nRound " + rounds + ": Enter your guess between 1-100:");

                while (attempts < 10 && !GuessedCorrectly) {
                    System.out.print("Enter your guess: ");
                    try {
                        int userGuess = scanner.nextInt();
                        attempts++;

                        if (userGuess == numberToGuess) {
                            System.out.println("Wonderful , Your guess is correct");
                            GuessedCorrectly = true;
                            totalScore += 10 - attempts;
                        } else if (userGuess < numberToGuess) {
                            System.out.println("Your guess is too low.");
                        } else {
                            System.out.println("Your guess is too high.");
                        }
                    } catch (Exception e) {
                        System.out.println("Invalid guess. Please enter a valid number between 1 and 100.");
                        scanner.next();
                    }
                }

                if (!GuessedCorrectly) {
                    System.out.println("Sorry, you've used all attempts. The correct number was: " + numberToGuess);
                }

                System.out.println("Your score after round " + rounds + ": " + totalScore);
                System.out.print("Do you want to play another round? (yes/no): ");
                playAgain = scanner.next().equalsIgnoreCase("yes");
            }

            System.out.println("Thank you  for playing the game ! Your final score is: " + totalScore);
            scanner.close();
        }
    }

