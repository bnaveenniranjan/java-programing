import java.util.Scanner;

// Interface definition
interface Calculator {
    double add(double num1, double num2);
    double sub(double num1, double num2);
    double mul(double num1, double num2);
    double div(double num1, double num2);
}

// Implementation class
class BasicCalculator implements Calculator {
    @Override
    public double add(double num1, double num2) {
        return num1 + num2;
    }

    @Override
    public double sub(double num1, double num2) {
        return num1 - num2;
    }

    @Override
    public double mul(double num1, double num2) {
        return num1 * num2;
    }

    @Override
    public double div(double num1, double num2) {
        if (num2 == 0) {
            throw new ArithmeticException("Cannot divide by zero");
        }
        return num1 / num2;
    }
}

// Example usage
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        BasicCalculator calculator = new BasicCalculator();

        System.out.print("Enter first number: ");
        double num1 = scanner.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = scanner.nextDouble();

        double resultAdd = calculator.add(num1, num2);
        System.out.println("Addition result: " + resultAdd);

        double resultSub = calculator.sub(num1, num2);
        System.out.println("Subtraction result: " + resultSub);

        double resultMul = calculator.mul(num1, num2);
        System.out.println("Multiplication result: " + resultMul);

        double resultDiv = calculator.div(num1, num2);
        System.out.println("Division result: " + resultDiv);

        scanner.close(); // closing scanner to prevent resource leak
    }
}
