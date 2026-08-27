# RockPaper
import java.util.Scanner;
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Random random = new Random();

        String[] choices = {"rock", "paper", "scissors"};

        System.out.print("Enter rock, paper, or scissors: ");
        String user = sc.nextLine().toLowerCase();

        String computer = choices[random.nextInt(3)];

        System.out.println("Computer chose: " + computer);

        if (!user.equals("rock") && !user.equals("paper") && !user.equals("scissors")) {
            System.out.println("Invalid choice!");
        } 
        else if (user.equals(computer)) {
            System.out.println("It's a tie!");
        } 
        else if ((user.equals("rock") && computer.equals("scissors")) ||
                 (user.equals("paper") && computer.equals("rock")) ||
                 (user.equals("scissors") && computer.equals("paper"))) {
            System.out.println("You win!");
        } 
        else {
            System.out.println("Computer wins!");
        }

        sc.close();
    }
}
