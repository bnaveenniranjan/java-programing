class InvalidDecimalNumberException extends Exception {
    public InvalidDecimalNumberException() {
        super("Invalid decimal number entered.");
    }
}

public class InvalidDecimalNumberExample {
    public static void main(String[] args) {
        try {
            double userInput = getUserInput();
            if (!isValidDecimal(userInput)) {
                throw new InvalidDecimalNumberException();
            }
            System.out.println("User input: " + userInput);
        } catch (InvalidDecimalNumberException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }

    public static double getUserInput() {
        // Simulating user input, replace this with your actual user input mechanism
        return -5.5; // Example user input (invalid decimal number)
    }

    public static boolean isValidDecimal(double number) {
        // Check if the number is a valid decimal
        return Double.isFinite(number);
    }
}
