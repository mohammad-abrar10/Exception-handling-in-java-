# Exception-handling-in-java-
import java.util.Scanner;

public class SimpleExceptionHandling {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Enter numerator: ");
            int numerator = scanner.nextInt();

            System.out.print("Enter denominator: ");
            int denominator = scanner.nextInt();

            int result = divide(numerator, denominator);
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.err.println("Error: Division by zero is not allowed.");
        } catch (Exception e) {
            System.err.println("An unexpected error occurred: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }

    public static int divide(int numerator, int denominator) {
        return numerator / denominator;
    }
}
