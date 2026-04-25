# JavaLabCS23.252
[#Program1:Create a class with four methods: Addition, Subtraction, Multiplication, and Division. Now, test all four methods in the public static void main.]
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
#program5
import java.util.Scanner;

class PyramidStars {

    int n;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of rows: ");
        n = sc.nextInt();
    }

    void printPyramid() {
        for (int i = 1; i <= n; i++) {

            for (int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }

            for (int k = 1; k <= (2 * i - 1); k++) {
                System.out.print("*");
            }

            System.out.println();
        }
    }

    public static void main(String[] args) {
        PyramidStars obj = new PyramidStars();
        obj.input();
        obj.printPyramid();
    }
}
Output:
<img width="318" height="236" alt="image" src="https://github.com/user-attachments/assets/439ef5b6-c6ec-4dc8-adba-c3816e983bcd" />
#program6
import java.util.Scanner;

class Distance {
    int meters;
    int centimeters;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter meters: ");
        meters = sc.nextInt();
        System.out.print("Enter centimeters: ");
        centimeters = sc.nextInt();
    }

    Distance add(Distance d) {
        Distance sum = new Distance();
        sum.centimeters = this.centimeters + d.centimeters;
        sum.meters = this.meters + d.meters + sum.centimeters / 100;
        sum.centimeters = sum.centimeters % 100;  
        return sum;
    }

    void display() {
        System.out.println("Distance = " + meters + " meters and " + centimeters + " centimeters");
    }

    public static void main(String[] args) {
        Distance d1 = new Distance();
        Distance d2 = new Distance();

        System.out.println("Enter first distance:");
        d1.input();

        System.out.println("Enter second distance:");
        d2.input();

        Distance sum = d1.add(d2);

        System.out.print("Sum of distances: ");
        sum.display();
    }
}
Output:
<img width="519" height="253" alt="image" src="https://github.com/user-attachments/assets/b68792f5-86b8-4c5f-9c79-e6306a7d5640" />
#program7
import java.util.Scanner;

class Distance {
    int meters;
    int centimeters;
    int millimeters;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter meters: ");
        meters = sc.nextInt();
        System.out.print("Enter centimeters: ");
        centimeters = sc.nextInt();
        System.out.print("Enter millimeters: ");
        millimeters = sc.nextInt();
    }

    Distance add(Distance d) {
        Distance sum = new Distance();

        sum.millimeters = this.millimeters + d.millimeters;
        sum.centimeters = this.centimeters + d.centimeters + sum.millimeters / 10; // 10 mm = 1 cm
        sum.millimeters = sum.millimeters % 10;

        sum.meters = this.meters + d.meters + sum.centimeters / 100; // 100 cm = 1 m
        sum.centimeters = sum.centimeters % 100;

        return sum;
    }

    void display() {
        System.out.println("Distance = " + meters + " meters, " + centimeters + " centimeters, and " + millimeters + " millimeters");
    }

    public static void main(String[] args) {
        Distance d1 = new Distance();
        Distance d2 = new Distance();

        System.out.println("Enter first distance:");
        d1.input();

        System.out.println("Enter second distance:");
        d2.input();

        Distance sum = d1.add(d2);

        System.out.print("Sum of distances: ");
        sum.display();
    }
}
Output:
<img width="526" height="325" alt="image" src="https://github.com/user-attachments/assets/321ebb9e-16bf-4266-9667-c057ad88a3e6" />
#program8
import java.util.Scanner;

class Time {
    int hours;
    int minutes;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter hours: ");
        hours = sc.nextInt();
        System.out.print("Enter minutes: ");
        minutes = sc.nextInt();
    }

    Time add(Time t) {
        Time sum = new Time();
        sum.minutes = this.minutes + t.minutes;
        sum.hours = this.hours + t.hours + sum.minutes / 60; // 60 min = 1 hr
        sum.minutes = sum.minutes % 60;
        return sum;
    }

    void display() {
        System.out.println("Time = " + hours + " hours and " + minutes + " minutes");
    }

    public static void main(String[] args) {
        Time t1 = new Time();
        Time t2 = new Time();

        System.out.println("Enter first time:");
        t1.input();

        System.out.println("Enter second time:");
        t2.input();

        Time sum = t1.add(t2);

        System.out.print("Sum of times: ");
        sum.display();
    }
}
Output:
<img width="421" height="286" alt="image" src="https://github.com/user-attachments/assets/79c51daf-0305-477f-a32d-3588c765c646" />
