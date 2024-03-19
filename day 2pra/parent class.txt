class Parent {
    void even() {
        System.out.println("Printing even numbers from 1 to 20:");
        for (int i = 1; i <= 20; i++) {
            if (i % 2 == 0) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }

    void odd() {
        System.out.println("Printing odd numbers from 1 to 20:");
        for (int i = 1; i <= 20; i++) {
            if (i % 2 != 0) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }

    void prime() {
        System.out.println("Printing prime numbers from 1 to 20:");
        for (int i = 1; i <= 20; i++) {
            boolean isPrime = true;
            if (i == 1) {
                isPrime = false;
            } else {
                for (int j = 2; j <= i / 2; j++) {
                    if (i % j == 0) {
                        isPrime = false;
                        break;
                    }
                }
            }
            if (isPrime) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }
}

class Child extends Parent {
    @Override
    void even() {
        System.out.println("Printing even numbers from 1 to 30:");
        for (int i = 1; i <= 30; i++) {
            if (i % 2 == 0) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }

    @Override
    void odd() {
        System.out.println("Printing odd numbers from 1 to 30:");
        for (int i = 1; i <= 30; i++) {
            if (i % 2 != 0) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }

    @Override
    void prime() {
        System.out.println("Printing prime numbers from 1 to 30:");
        for (int i = 1; i <= 30; i++) {
            boolean isPrime = true;
            if (i == 1) {
                isPrime = false;
            } else {
                for (int j = 2; j <= i / 2; j++) {
                    if (i % j == 0) {
                        isPrime = false;
                        break;
                    }
                }
            }
            if (isPrime) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {
        Child child = new Child();
        child.even();
        child.odd();
        child.prime();
    }
}
