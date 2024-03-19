import java.util.Scanner;

// Interface for sum
interface Summable {
    double sum(double[] numbers);
}

// Interface for average
interface Averagable {
    double avg(double[] numbers);
}

// Interface for percentage
interface Percentagable {
    double percentage(double obtained, double total);
}

// Implementation class
class CalculatorImpl implements Summable, Averagable, Percentagable {

    @Override
    public double sum(double[] numbers) {
        double total = 0;
        for (double num : numbers) {
            total += num;
        }
        return total;
    }

    @Override
    public double avg(double[] numbers) {
        double total = sum(numbers);
        return total / numbers.length;
    }

    @Override
    public double percentage(double obtained, double total) {
        return (obtained / total) * 100;
    }
}

// Example usage
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        CalculatorImpl calculator = new CalculatorImpl();

        System.out.print("Enter the number of elements: ");
        int count = scanner.nextInt();
        double[] numbers = new double[count];
        for (int i = 0; i < count; i++) {
            System.out.print("Enter number " + (i + 1) + ": ");
            numbers[i] = scanner.nextDouble();
        }

        double total = calculator.sum(numbers);
        double average = calculator.avg(numbers);

        System.out.println("Sum: " + total);
        System.out.println("Average: " + average);

        System.out.print("Enter the marks obtained: ");
        double obtainedMarks = scanner.nextDouble();
        System.out.print("Enter the total marks: ");
        double totalMarks = scanner.nextDouble();

        double percentage = calculator.percentage(obtainedMarks, totalMarks);
        System.out.println("Percentage: " + percentage + "%");

        scanner.close();
    }
}
