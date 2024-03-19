public class Main {
    static int staticVariable = 10;

    static void staticMethod() {
        System.out.println("This is a static method.");
    }

    static {
        System.out.println("This is a static block.");
    }

    static class StaticNestedClass {
        void display() {
            System.out.println("This is a static nested class.");
        }
    }

    public static void main(String[] args) {
        System.out.println("Value of staticVariable: " + staticVariable);
        staticMethod();
        StaticNestedClass nestedObject = new StaticNestedClass();
        nestedObject.display();
    }
}
