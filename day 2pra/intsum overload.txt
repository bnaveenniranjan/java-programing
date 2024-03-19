public class OverloadingExample {

    // Overloading by increasing and decreasing the number of parameters
    int sum(int a, int b) {
        return a + b;
    }

    int sum(int a, int b, int c) {
        return a + b + c;
    }

    // Overloading by changing the data types of parameters
    double sum(double a, double b) {
        return a + b;
    }

    // Overloading by interchanging the parameters
    int sum(String message, int a) {
        System.out.println(message);
        return a;
    }

    int sum(int a, String message) {
        System.out.println(message);
        return a;
    }

    public static void main(String[] args) {
        OverloadingExample obj = new OverloadingExample();

        // Testing overloads
        System.out.println("Sum of 5 and 10: " + obj.sum(5, 10));
        System.out.println("Sum of 5, 10, and 15: " + obj.sum(5, 10, 15));
        System.out.println("Sum of 5.5 and 10.5: " + obj.sum(5.5, 10.5));
        System.out.println("Return 10: " + obj.sum("Returning 10:", 10));
        System.out.println("Return 20: " + obj.sum(20, "Returning 20:"));
    }
}
