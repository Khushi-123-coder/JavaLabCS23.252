# JavaLabCS23.252
Program1:Create a class with four methods: Addition, Subtraction, Multiplication, and Division. Now, test all four methods in the public static void main.
[Go to Program 1](#program1)
Write a Program to test for loop, while loop, do while loop for Problem 1 (#program2)
Write a Program using if-else to print the grade of input marks.(#program3)
Write a Program in Java using objects and classes to get the square of stars for dynamic width and height.(#program4)
Write a Program in Java using objects and classes to get the pyramid of stars or triangle of stars.(#program5)
Write a Program in Java using OOPs concept for the addition of two distances where each distance is given in metres and centimetres.(#program6)
Write a Program in Java using OOPs concept for the addition of two distances where each distance is given in metres, centimetres, and millimeters.(#program7)
Write a Program in Java using OOPs concept for the addition of two times, where each time is given in hours and minutes.(#program8)
Write a Program in Java using OOPs concept for the addition of two times, where each time is given in hours, minutes, and seconds.(#program9)
Write a class with four methods for a 1-dimensional array.(Input, output 1,out2, reverse).(#program10)
Write a class with multiple methods to perform matrix operations (transpose, addition, sum of rows, sum of columns, sum of diagonal).(#program11)
Collect the code from the internet for any five programs in the C language and convert them to Java. (Factorial).(#program12a)
Collect the code from the internet for any five programs of the C language and convert them to Java. (Armstrong).(#program12b)
Collect the code from the internet for any five programs of the C language and convert them to Java. (Palindrome).(#program12c)
Collect the code from the internet for any five programs of the C language and convert them to Java. (Fibonacci).(#program12d)
Collect the code from the internet for any five programs of the C language and convert them to Java. (Pattern).(#program12e)
Write a program using three classes to print 1–100, 1–100, 1–100 without a thread, and analyse the output, and repeat the same program using the Runnable interface.(#program13)
Write a program using three classes to print 1–100, 1–100, 1–100 with a thread and analyse the output, and repeat the same program using the Runnable interface.(#program14)
Program 15: Using the concept of multithreading, the output of all three threads must be synchronised (use the join method).(#program15)
Program 16: Addition of 2 numbers using Swing.(#program16)
Program 17: Make one calculator in Swing.(#program17)
Program 18: Matrix Addition using swing class.(#program18)
Program 19: Create one JFrame with 10 buttons on it. After clicking on each button, a new structure is created (Circle, oval, rectangle, etc).(#program19)
Program 20: Just using mouse events creates a frame like a paint brush with selection of colour and width.(#program20)
Program 21: Create a package of any 5 classes of your choice and import it.(#program21)
Program 22: Create one package and a sub-package, import and test it.(#program22)
Program 23: Create one small array of size 5, apply array out of bounds exception using try-catch, give a proper message in catch, and demonstrate the exception exactly in the same fashion. Demonstrate arithmetic exception also.(#program23)
Program 24: To test the range of age of one student, write a program using a user-defined exception.(#program24)
Program 25: File Handling Programs (given in the PPT).(#program25)
Program 26: Inheritance Programs, using interface and abstract classes.(#program26)
Program 27: Make a registration form with 10 elements and send the data to the database (use JDBC connectivity).(#program27)
#program1
public class Calculator {

    // Method for Addition
    public int add(int a, int b) {
        return a + b;
    }

    // Method for Subtraction
    public int subtract(int a, int b) {
        return a - b;
    }

    // Method for Multiplication
    public int multiply(int a, int b) {
        return a * b;
    }

    // Method for Division
    public double divide(int a, int b) {
        if (b == 0) {
            System.out.println("Cannot divide by zero");
            return 0;
        }
        return (double) a / b;
    }

    // Main method to test all methods
    public static void main(String[] args) {
        Calculator calc = new Calculator();

        int num1 = 20;
        int num2 = 10;

        System.out.println("Addition: " + calc.add(num1, num2));
        System.out.println("Subtraction: " + calc.subtract(num1, num2));
        System.out.println("Multiplication: " + calc.multiply(num1, num2));
        System.out.println("Division: " + calc.divide(num1, num2));
    }
}
Output:
<img width="508" height="107" alt="image" src="https://github.com/user-attachments/assets/fb34402d-23e5-4895-a2a6-82cef31a4730" />
#program2
class LoopTest {
    public static void main(String[] args) {

        System.out.println("Using for loop:");
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }

        System.out.println("\nUsing while loop:");
        int j = 1;
        while (j <= 5) {
            System.out.println(j);
            j++;
        }

        System.out.println("\nUsing do-while loop:");
        int k = 1;
        do {
            System.out.println(k);
            k++;
        } while (k <= 5);
    }
}
Output:
<img width="375" height="561" alt="image" src="https://github.com/user-attachments/assets/379fc8a3-9c8b-47b4-8f0b-9dbbc283edfa" />
#program3
import java.util.Scanner;

class GradeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System. out.print("Enter marks: ");
        int marks = sc.nextInt();

        if (marks >= 90) {
            System.out.println("Grade: A");
        } else if (marks >= 75) {
            System.out.println("Grade: B");
        } else if (marks >= 60) {
            System.out.println("Grade: C");
        } else if (marks >= 50) {
            System.out.println("Grade: D");
        } else {
            System.out.println("Grade: F");
        }

        sc.close();
    }
}
Output:
<img width="317" height="171" alt="image" src="https://github.com/user-attachments/assets/8f74cb97-252a-44c4-85bb-c548d1b7e678" />
#program4
import java.util.Scanner;

class SquareStars {

    int width, height;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter width: ");
        width = sc.nextInt();
        System.out.print("Enter height: ");
        height = sc.nextInt();
    }

    void printSquare() {
        for (int i = 1; i <= height; i++) {
            for (int j = 1; j <= width; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        SquareStars obj = new SquareStars();
        obj.input();
        obj.printSquare();
    }
}
Output:
<img width="312" height="383" alt="image" src="https://github.com/user-attachments/assets/2ee8716b-d93b-470a-a093-e94ae60e6249" />
