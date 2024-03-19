class MyClass {
    int a, b;

    // Default constructor
    MyClass() {
        a = 10;
        b = 15;
    }

    // Parameterized constructor
    MyClass(int a, int b) {
        this.a = a;
        this.b = b;
    }

    // Method to display values of a and b
    void disp() {
        System.out.println("a = " + a + ", b = " + b);
    }

    public static void main(String[] args) {
        // Creating an object using default constructor
        MyClass obj1 = new MyClass();
        System.out.println("Values initialized using default constructor:");
        obj1.disp();

        // Creating an object using parameterized constructor
        MyClass obj2 = new MyClass(20, 25);
        System.out.println("Values initialized using parameterized constructor:");
        obj2.disp();
    }
}
