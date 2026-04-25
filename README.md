# JavaLabCS23.252
## Programs List

[Program 1: Calculator Methods](#program1)  

[Program 2: Loops Test](#program2)  

[Program 3: Grade using If-Else](#program3)

[Program 4: Square of Stars](#program4)

[Program 5: Pyramid of Stars](#program5)

[Program 6: Distance (m, cm)](#program6)

[Program 7: Distance (m, cm, mm)](#program7)

[Program 8: Time (hours, minutes)](#program8)

[Program 9: Time (h, m, s)](#program9)

[Program 10: 1D Array Methods](#program10)

[Program 11: Matrix Operations](#program11)

[Program 12a: Factorial](#program12a)

[Program 12b: Armstrong](#program12b)

[Program 12c: Palindrome](#program12c)

[Program 12d: Fibonacci](#program12d)

[Program 12e: Pattern](#program12e)

[Program 13: Without Thread](#program13)

[Program 14: With Thread](#program14)

[Program 15: Thread Synchronization](#program15)

[Program 16: Swing Addition](#program16)

[Program 17: Swing Calculator](#program17)

[Program 18: Matrix Addition Swing](#program18)

[Program 19: JFrame Shapes](#program19)

[Program 20: Paint Brush (Mouse Events)](#program20)

[Program 21: Package (5 Classes)](#program21)

[Program 22: Package + Subpackage](#program22)

[Program 23: Exception Handling](#program23)

[Program 24: User-defined Exception](#program24)

[Program 25: File Handling](#program25)

[Program 26: Inheritance + Interface](#program26)

[Program 27: Registration Form (JDBC)](#program27)

##program1(#program1)

```java
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
```
Output:
<img width="508" height="107" alt="image" src="https://github.com/user-attachments/assets/fb34402d-23e5-4895-a2a6-82cef31a4730" />
#program2
```java
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
```
Output:
<img width="375" height="561" alt="image" src="https://github.com/user-attachments/assets/379fc8a3-9c8b-47b4-8f0b-9dbbc283edfa" />
#program3
```java
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
```
Output:
<img width="317" height="171" alt="image" src="https://github.com/user-attachments/assets/8f74cb97-252a-44c4-85bb-c548d1b7e678" />
#program4
```java
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
```
Output:
<img width="312" height="383" alt="image" src="https://github.com/user-attachments/assets/2ee8716b-d93b-470a-a093-e94ae60e6249" />
#program5
```java
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
```
Output:
<img width="318" height="236" alt="image" src="https://github.com/user-attachments/assets/439ef5b6-c6ec-4dc8-adba-c3816e983bcd" />
#program6
```java
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
```
Output:
<img width="519" height="253" alt="image" src="https://github.com/user-attachments/assets/b68792f5-86b8-4c5f-9c79-e6306a7d5640" />
#program7
```java
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
```
Output:
<img width="526" height="325" alt="image" src="https://github.com/user-attachments/assets/321ebb9e-16bf-4266-9667-c057ad88a3e6" />
#program8
```java
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
```
Output:
<img width="421" height="286" alt="image" src="https://github.com/user-attachments/assets/79c51daf-0305-477f-a32d-3588c765c646" />
#program9
```java
import java.util.Scanner;

class Time {
    int hours;
    int minutes;
    int seconds;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter hours: ");
        hours = sc.nextInt();
        System.out.print("Enter minutes: ");
        minutes = sc.nextInt();
        System.out.print("Enter seconds: ");
        seconds = sc.nextInt();
    }

    Time add(Time t) {
        Time sum = new Time();

        sum.seconds = this.seconds + t.seconds;
        sum.minutes = this.minutes + t.minutes + sum.seconds / 60;
        sum.seconds = sum.seconds % 60;

        sum.hours = this.hours + t.hours + sum.minutes / 60;
        sum.minutes = sum.minutes % 60;

        return sum;
    }

    void display() {
        System.out.println("Time = " + hours + " hours, " + minutes + " minutes, " + seconds + " seconds");
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
```
Ouptput:
<img width="513" height="307" alt="image" src="https://github.com/user-attachments/assets/48a05f3c-0436-4e2a-93ba-e9e575ff41cf" />
#program10
```java
import java.util.Scanner;

class OneDArray {
    int arr[];
    int n;

    void input() {
        Scanner sc = new Scanner(System.in);
        System. out.print("Enter size of array: ");
        n = sc.nextInt();

        arr = new int[n];
        System.out.println("Enter elements:");

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
    }

    void output1() {
        System.out.println("Array elements:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    void output2() {
        System.out.println("Even elements:");
        for (int i = 0; i < n; i++) {
            if (arr[i] % 2 == 0) {
                System.out.print(arr[i] + " ");
            }
        }
        System.out.println();
    }

    void reverse() {
        System.out.println("Reversed array:");
        for (int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {
        OneDArray obj = new OneDArray();
        obj.input();
        obj.output1();
        obj.output2();
        obj.reverse();
    }
}
```
Output:
<img width="429" height="320" alt="image" src="https://github.com/user-attachments/assets/55a06bb5-6526-454e-8a78-ef2325ecfbc8" />
#program11
```java
import java.util.Scanner;

class MatrixOperations {
    int a[][], b[][];
    int r, c;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter rows and columns: ");
        r = sc.nextInt();
        c = sc.nextInt();

        a = new int[r][c];
        b = new int[r][c];

        System.out.println("Enter first matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                a[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter second matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                b[i][j] = sc.nextInt();
            }
        }
    }

    void addition() {
        System.out.println("Matrix Addition:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                System.out.print((a[i][j] + b[i][j]) + " ");
            }
            System.out.println();
        }
    }

    void transpose() {
        System.out.println("Transpose of first matrix:");
        for (int i = 0; i < c; i++) {
            for (int j = 0; j < r; j++) {
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }

    void sumRows() {
        System. out.println("Sum of rows:");
        for (int i = 0; i < r; i++) {
            int sum = 0;
            for (int j = 0; j < c; j++) {
                sum += a[i][j];
            }
            System.out.println("Row " + i + ": " + sum);
        }
    }

    void sumColumns() {
        System. out.println("Sum of columns:");
        for (int j = 0; j < c; j++) {
            int sum = 0;
            for (int i = 0; i < r; i++) {
                sum += a[i][j];
            }
            System.out.println("Column " + j + ": " + sum);
        }
    }

    void sumDiagonal() {
        int sum = 0;
        for (int i = 0; i < r; i++) {
            sum += a[i][i]; // main diagonal
        }
        System.out.println("Sum of diagonal: " + sum);
    }

    public static void main(String[] args) {
        MatrixOperations obj = new MatrixOperations();
        obj.input();
        obj.addition();
        obj.transpose();
        obj.sumRows();
        obj.sumColumns();
        obj.sumDiagonal();
    }
}
```
Output:
<img width="489" height="624" alt="image" src="https://github.com/user-attachments/assets/07dd6f50-163e-4515-9d6c-6220a910f661" />
#program12a
```java
import java.util.Scanner;

class Factorial {
    public static void main(String[] args) {
        int n, fact = 1;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        n = sc.nextInt();

        for (int i = 1; i <= n; i++) {
            fact *= i;
        }

        System.out.println("Factorial = " + fact);
    }
}
```
Output:
<img width="374" height="136" alt="image" src="https://github.com/user-attachments/assets/be5e909f-b19c-4c5d-8137-ca25de87f27e" />
#program12b
```java
import java.util.Scanner;

class Armstrong {
    public static void main(String[] args) {
        int n, temp, rem, sum = 0;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        n = sc.nextInt();

        temp = n;

        while (n > 0) {
            rem = n % 10;
            sum += rem * rem * rem;
            n = n / 10;
        }

        if (temp == sum)
            System. out.println("Armstrong Number");
        else
            System. out.println("Not an Armstrong Number");
    }
}
```
output:
<img width="408" height="152" alt="image" src="https://github.com/user-attachments/assets/75eb2ae6-aadd-473b-838c-1fae3a37b9b8" />





