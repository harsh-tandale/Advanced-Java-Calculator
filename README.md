import java.util.Scanner;

public class AdvancedCalculator {

    // Method for Addition
    static double add(double a, double b) {
        return a + b;
    }

    // Method for Subtraction
    static double subtract(double a, double b) {
        return a - b;
    }

    // Method for Multiplication
    static double multiply(double a, double b) {
        return a * b;
    }

    // Method for Division
    static double divide(double a, double b) {
        if (b == 0) {
            System.out.println("Error! Division by zero.");
            return 0;
        }
        return a / b;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int choice;
        double num1, num2;
        char again;

        do {
            System.out.println("\n===== ADVANCED CALCULATOR =====");
            System.out.println("1. Addition (+)");
            System.out.println("2. Subtraction (-)");
            System.out.println("3. Multiplication (*)");
            System.out.println("4. Division (/)");
            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            System.out.print("Enter two numbers: ");
            num1 = sc.nextDouble();
            num2 = sc.nextDouble();

            switch (choice) {
                case 1:
                    System.out.println("Result = " + add(num1, num2));
                    break;

                case 2:
                    System.out.println("Result = " + subtract(num1, num2));
                    break;

                case 3:
                    System.out.println("Result = " + multiply(num1, num2));
                    break;

                case 4:
                    System.out.println("Result = " + divide(num1, num2));
                    break;

                default:
                    System.out.println("Invalid choice!");
            }

            System.out.print("\nDo you want to continue? (y/n): ");
            again = sc.next().charAt(0);

        } while (again == 'y' || again == 'Y');

        System.out.println("Thank you for using the Calculator 😊");
        sc.close();
    }
}
