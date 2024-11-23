import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter the number of rows and columns
        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();
        System.out.print("Enter the number of columns: ");
        int cols = scanner.nextInt();

        // Create and initialize the 2D array
        int[][] table = new int[rows][cols];

        // Populate the array using a nested for loop
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                table[i][j] = i * j;
            }
        }

        // Print the table to display the multiplication pattern
        System.out.println("\nMultiplication Table:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(table[i][j] + "\t"); // \t is used for tab spacing
            }
            System.out.println(); // Move to the next line after each row
        }

        // Close the scanner
        scanner.close();
    }
}
