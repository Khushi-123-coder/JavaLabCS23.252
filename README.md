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

<h2 id="program1">Program 1</h2>

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
<h2 id="program2">Program 2</h2>

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

<h2 id="program3">Program 3</h2>

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

<h2 id="program4">Program 4</h2>

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

<h2 id="program5">Program 5</h2>

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



<h2 id="program6">Program 6</h2>

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

<h2 id="program7">Program 7</h2>

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

<h2 id="program8">Program 8</h2>

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

<h2 id="program9">Program 9</h2>

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

<h2 id="program10">Program 10</h2>

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

<h2 id="program11">Program 11</h2>

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

<h2 id="program12a">Program 12a</h2>
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

<h2 id="program12b">Program 12b</h2>

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

<h2 id="program12c">Program 12c</h2>

```java

import java.util.Scanner;

class Palindrome {
    public static void main(String[] args) {
        int n, rev = 0, rem, temp;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        n = sc.nextInt();

        temp = n;

        while (n > 0) {
            rem = n % 10;
            rev = rev * 10 + rem;
            n = n / 10;
        }

        if (temp == rev)
            System. out.println("Palindrome Number");
        else
            System. out.println("Not a Palindrome Number");
    }
}

```
Output:
<img width="463" height="141" alt="image" src="https://github.com/user-attachments/assets/b540204a-7ac0-4c98-ba2f-ee5a240f0b3b" />

<h2 id="program12d">Program 12d</h2>

```java

import java.util.Scanner;

class Fibonacci {
    public static void main(String[] args) {
        int n, a = 0, b = 1, c;

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of terms: ");
        n = sc.nextInt();

        System.out.println("Fibonacci Series:");
        System.out.print(a + " " + b + " ");

        for (int i = 3; i <= n; i++) {
            c = a + b;
            System.out.print(c + " ");
            a = b;
            b = c;
        }
    }
}

```
Output:
<img width="924" height="157" alt="image" src="https://github.com/user-attachments/assets/69b9976c-c027-41d7-9a3d-a860c4348571" />

<h2 id="program12e">Program 12e</h2>

```java
class Pattern {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}

```
Output:
<img width="483" height="210" alt="image" src="https://github.com/user-attachments/assets/ad66edcb-a949-4e74-bcaa-5e50e4cdaa57" />

<h2 id="program13">Program 13</h2>

```java

class PrintOneToHundred {
    void display() {
        System. out.println("Printing 1 to 100:");
        for (int i = 1; i <= 100; i++) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

class PrintHundredToOne {
    void display() {
        System. out.println("Printing 100 to 1:");
        for (int i = 100; i >= 1; i--) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

class PrintOneToHundredAgain {
    void display() {
        System. out.println("Printing 1 to 100 again:");
        for (int i = 1; i <= 100; i++) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {
        PrintOneToHundred obj1 = new PrintOneToHundred();
        PrintHundredToOne obj2 = new PrintHundredToOne();
        PrintOneToHundredAgain obj3 = new PrintOneToHundredAgain();

        obj1.display();
        obj2.display();
        obj3.display();
    }
}

```
Output:
<img width="919" height="564" alt="image" src="https://github.com/user-attachments/assets/6bc7afe9-1658-4a4c-a995-7b782277f712" />

<h2 id="program14">Program 14</h2>

```java

class ThreadOne extends Thread {
    public void run() {
        System. out.println("Thread 1: Printing 1 to 100");
        for (int i = 1; i <= 100; i++) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

class ThreadTwo extends Thread {
    public void run() {
        System. out.println("Thread 2: Printing 100 to 1");
        for (int i = 100; i >= 1; i--) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

class ThreadThree extends Thread {
    public void run() {
        System. out.println("Thread 3: Printing 1 to 100");
        for (int i = 1; i <= 100; i++) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {

        ThreadOne t1 = new ThreadOne();
        ThreadTwo t2 = new ThreadTwo();
        ThreadThree t3 = new ThreadThree();

        t1.start();
        t2.start();
        t3.start();
    }
}

```
Output:
<img width="908" height="545" alt="image" src="https://github.com/user-attachments/assets/218519a8-77c7-44b4-9879-5d0cfc793bbc" />

<h2 id="program15">Program 15</h2>

```java

class ThreadOne extends Thread {
    public void run() {
        System. out.println("Thread 1: Printing 1 to 100");
        for (int i = 1; i <= 100; i++) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

class ThreadTwo extends Thread {
    public void run() {
        System. out.println("Thread 2: Printing 100 to 1");
        for (int i = 100; i >= 1; i--) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

class ThreadThree extends Thread {
    public void run() {
        System. out.println("Thread 3: Printing 1 to 100");
        for (int i = 1; i <= 100; i++) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {

        ThreadOne t1 = new ThreadOne();
        ThreadTwo t2 = new ThreadTwo();
        ThreadThree t3 = new ThreadThree();

        try {
            t1.start();
            t1.join();   

            t2.start();
            t2.join();  

            t3.start();
            t3.join();  

        } catch (InterruptedException e) {
            System. out.println("Exception: " + e);
        }
    }
}

```
Output:
<img width="928" height="582" alt="image" src="https://github.com/user-attachments/assets/d3841595-50eb-465b-b5f2-e0fa932f8862" />

<h2 id="program16">Program 16</h2>

```java

import javax.swing.*;
import java.awt.event.*;

public class Main extends JFrame implements ActionListener {
    JLabel l1, l2, l3;
    JTextField t1, t2, t3;
    JButton b1;

    Main() {
        l1 = new JLabel("Enter First Number:");
        l2 = new JLabel("Enter Second Number:");
        l3 = new JLabel("Result:");

        t1 = new JTextField();
        t2 = new JTextField();
        t3 = new JTextField();
        t3.setEditable(false);

        b1 = new JButton("Add");
        b1.addActionListener(this);

        l1.setBounds(50, 50, 150, 30);
        t1.setBounds(200, 50, 150, 30);

        l2.setBounds(50, 100, 150, 30);
        t2.setBounds(200, 100, 150, 30);

        l3.setBounds(50, 150, 150, 30);
        t3.setBounds(200, 150, 150, 30);

        b1.setBounds(140, 220, 100, 30);

        add(l1); add(t1);
        add(l2); add(t2);
        add(l3); add(t3);
        add(b1);

        setTitle("Addition of Two Numbers");
        setSize(450, 350);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e) {
        int num1 = Integer.parseInt(t1.getText());
        int num2 = Integer.parseInt(t2.getText());
        int sum = num1 + num2;
        t3.setText(String.valueOf(sum));
    }

    public static void main(String[] args) {
        new Main();
    }
}

```
Output:
<img width="550" height="431" alt="image" src="https://github.com/user-attachments/assets/9024b5b7-99a7-457b-b4bf-7af5bb022bb2" />

<h2 id="program17">Program 17</h2>

```java

import javax.swing.*;
import java.awt.event.*;

public class Main extends JFrame implements ActionListener {
    JLabel l1, l2, l3;
    JTextField t1, t2, t3;
    JButton b1, b2, b3, b4, b5;

    Main() {
        l1 = new JLabel("First Number:");
        l2 = new JLabel("Second Number:");
        l3 = new JLabel("Result:");

        t1 = new JTextField();
        t2 = new JTextField();
        t3 = new JTextField();
        t3.setEditable(false);

        b1 = new JButton("Add");
        b2 = new JButton("Sub");
        b3 = new JButton("Mul");
        b4 = new JButton("Div");
        b5 = new JButton("Clear");

        b1.addActionListener(this);
        b2.addActionListener(this);
        b3.addActionListener(this);
        b4.addActionListener(this);
        b5.addActionListener(this);

        l1.setBounds(50, 50, 100, 30);
        t1.setBounds(170, 50, 150, 30);

        l2.setBounds(50, 100, 100, 30);
        t2.setBounds(170, 100, 150, 30);

        l3.setBounds(50, 150, 100, 30);
        t3.setBounds(170, 150, 150, 30);

        b1.setBounds(30, 220, 70, 30);
        b2.setBounds(110, 220, 70, 30);
        b3.setBounds(190, 220, 70, 30);
        b4.setBounds(270, 220, 70, 30);
        b5.setBounds(150, 270, 80, 30);

        add(l1); add(t1);
        add(l2); add(t2);
        add(l3); add(t3);
        add(b1); add(b2); add(b3); add(b4); add(b5);

        setTitle("Calculator Using Swing");
        setSize(400, 380);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e) {
        try {
            double num1 = Double.parseDouble(t1.getText());
            double num2 = Double.parseDouble(t2.getText());
            double result = 0;

            if (e.getSource() == b1) {
                result = num1 + num2;
            } else if (e.getSource() == b2) {
                result = num1 - num2;
            } else if (e.getSource() == b3) {
                result = num1 * num2;
            } else if (e.getSource() == b4) {
                if (num2 == 0) {
                    JOptionPane.showMessageDialog(this, "Division by zero is not allowed");
                    return;
                }
                result = num1 / num2;
            } else if (e.getSource() == b5) {
                t1.setText("");
                t2.setText("");
                t3.setText("");
                return;
            }

            t3.setText(String.valueOf(result));

        } catch (NumberFormatException ex) {
            JOptionPane.showMessageDialog(this, "Please enter valid numbers");
        }
    }

    public static void main(String[] args) {
        new Main();
    }
}

```
Output:
<img width="494" height="469" alt="image" src="https://github.com/user-attachments/assets/e1101c41-ebed-4046-b014-679691f25386" />

<h2 id="program18">Program 18</h2>

```java

import javax.swing.*;
import java.awt.event.*;

public class Main extends JFrame implements ActionListener {

    JTextField a11, a12, a21, a22;
    JTextField b11, b12, b21, b22;
    JTextField r11, r12, r21, r22;
    JButton addBtn, clearBtn;

    Main() {
        setTitle("Matrix Addition (2x2)");
        setSize(420, 320);
        setLayout(null);

        JLabel la = new JLabel("Matrix A");
        la.setBounds(60, 10, 100, 20);
        add(la);

        a11 = new JTextField(); a11.setBounds(40, 40, 50, 30);
        a12 = new JTextField(); a12.setBounds(100, 40, 50, 30);
        a21 = new JTextField(); a21.setBounds(40, 80, 50, 30);
        a22 = new JTextField(); a22.setBounds(100, 80, 50, 30);

        JLabel lb = new JLabel("Matrix B");
        lb.setBounds(250, 10, 100, 20);
        add(lb);

        b11 = new JTextField(); b11.setBounds(230, 40, 50, 30);
        b12 = new JTextField(); b12.setBounds(290, 40, 50, 30);
        b21 = new JTextField(); b21.setBounds(230, 80, 50, 30);
        b22 = new JTextField(); b22.setBounds(290, 80, 50, 30);

        JLabel lr = new JLabel("Result");
        lr.setBounds(150, 120, 100, 20);
        add(lr);

        r11 = new JTextField(); r11.setBounds(120, 150, 50, 30); r11.setEditable(false);
        r12 = new JTextField(); r12.setBounds(180, 150, 50, 30); r12.setEditable(false);
        r21 = new JTextField(); r21.setBounds(120, 190, 50, 30); r21.setEditable(false);
        r22 = new JTextField(); r22.setBounds(180, 190, 50, 30); r22.setEditable(false);

        addBtn = new JButton("Add");
        clearBtn = new JButton("Clear");
        addBtn.setBounds(90, 240, 80, 30);
        clearBtn.setBounds(200, 240, 80, 30);

        addBtn.addActionListener(this);
        clearBtn.addActionListener(this);

        add(a11); add(a12); add(a21); add(a22);
        add(b11); add(b12); add(b21); add(b22);
        add(r11); add(r12); add(r21); add(r22);
        add(addBtn); add(clearBtn);

        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == addBtn) {
            try {
                int A11 = Integer.parseInt(a11.getText());
                int A12 = Integer.parseInt(a12.getText());
                int A21 = Integer.parseInt(a21.getText());
                int A22 = Integer.parseInt(a22.getText());

                int B11 = Integer.parseInt(b11.getText());
                int B12 = Integer.parseInt(b12.getText());
                int B21 = Integer.parseInt(b21.getText());
                int B22 = Integer.parseInt(b22.getText());

                r11.setText(String.valueOf(A11 + B11));
                r12.setText(String.valueOf(A12 + B12));
                r21.setText(String.valueOf(A21 + B21));
                r22.setText(String.valueOf(A22 + B22));

            } catch (NumberFormatException ex) {
                JOptionPane.showMessageDialog(this, "Enter valid integers");
            }
        }

        if (e.getSource() == clearBtn) {
            JTextField[] fields = {
                a11,a12,a21,a22, b11,b12,b21,b22, r11,r12,r21,r22
            };
            for (JTextField f: fields) f.setText("");
        }
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(() -> new Main());
    }
}

```
Output:
<img width="514" height="394" alt="image" src="https://github.com/user-attachments/assets/79e89323-7f4a-4437-8ef9-21293564710c" />

<h2 id="program19">Program 19</h2>

```java

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class ShapePanel extends JPanel {
    String shape = "";

    public void setShape(String shape) {
        this.shape = shape;
        repaint();
    }

    protected void paintComponent(Graphics g) {
        super.paintComponent(g);

        if (shape.equals("Line")) {
            g.drawLine(50, 50, 200, 50);
        } 
        else if (shape.equals("Rectangle")) {
            g.drawRect(50, 50, 120, 80);
        } 
        else if (shape.equals("Square")) {
            g.drawRect(50, 50, 100, 100);
        } 
        else if (shape.equals("Oval")) {
            g.drawOval(50, 50, 150, 100);
        } 
        else if (shape.equals("Circle")) {
            g.drawOval(50, 50, 100, 100);
        } 
        else if (shape.equals("RoundRect")) {
            g.drawRoundRect(50, 50, 150, 100, 30, 30);
        } 
        else if (shape.equals("Arc")) {
            g.drawArc(50, 50, 150, 100, 0, 180);
        } 
        else if (shape.equals("Triangle")) {
            int x[] = {100, 50, 150};
            int y[] = {50, 150, 150};
            g.drawPolygon(x, y, 3);
        } 
        else if (shape.equals("Polygon")) {
            int x[] = {100, 150, 130, 70, 50};
            int y[] = {50, 90, 150, 150, 90};
            g.drawPolygon(x, y, 5);
        } 
        else if (shape.equals("Clear")) {
        }
    }
}

public class Main extends JFrame implements ActionListener {
    JButton b1, b2, b3, b4, b5, b6, b7, b8, b9, b10;
    ShapePanel panel;

    Main() {
        setTitle("Shapes using 10 Buttons");
        setSize(700, 500);
        setLayout(null);

        panel = new ShapePanel();
        panel.setBounds(200, 30, 450, 400);
        panel.setBackground(Color.WHITE);

        b1 = new JButton("Line");
        b2 = new JButton("Rectangle");
        b3 = new JButton("Square");
        b4 = new JButton("Oval");
        b5 = new JButton("Circle");
        b6 = new JButton("RoundRect");
        b7 = new JButton("Arc");
        b8 = new JButton("Triangle");
        b9 = new JButton("Polygon");
        b10 = new JButton("Clear");

        JButton[] buttons = {b1, b2, b3, b4, b5, b6, b7, b8, b9, b10};

        int y = 30;
        for (JButton b: buttons) {
            b.setBounds(30, y, 130, 30);
            b.addActionListener(this);
            add(b);
            y += 35;
        }

        add(panel);

        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e) {
        String cmd = e.getActionCommand();
        panel.setShape(cmd);
    }

    public static void main(String[] args) {
        new Main();
    }
}

```
Output:
<img width="859" height="617" alt="image" src="https://github.com/user-attachments/assets/8487dd7e-050a-402a-b99c-593f4a43bc65" />

<h2 id="program20">Program 20</h2>

```java

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.util.ArrayList;

class DrawPoint {
    int x, y, size;
    Color color;

    DrawPoint(int x, int y, Color color, int size) {
        this.x = x;
        this.y = y;
        this.color = color;
        this.size = size;
    }
}

class PaintPanel extends JPanel implements MouseMotionListener {
    ArrayList<DrawPoint> points = new ArrayList<>();
    Color currentColor = Color.BLACK;
    int brushSize = 5;

    PaintPanel() {
        setBackground(Color.WHITE);
        addMouseMotionListener(this);
    }

    public void setCurrentColor(Color c) {
        currentColor = c;
    }

    public void setBrushSize(int size) {
        brushSize = size;
    }

    protected void paintComponent(Graphics g) {
        super.paintComponent(g);

        for (DrawPoint p: points) {
            g.setColor(p.color);
            g.fillOval(p.x, p.y, p.size, p.size);
        }
    }

    public void mouseDragged(MouseEvent e) {
        points.add(new DrawPoint(e.getX(), e.getY(), currentColor, brushSize));
        repaint();
    }

    public void mouseMoved(MouseEvent e) {
    }

    public void clearCanvas() {
        points.clear();
        repaint();
    }
}

//Main

public class Main extends JFrame implements ActionListener {
    JButton redBtn, blueBtn, greenBtn, blackBtn, clearBtn;
    JComboBox<String> widthBox;
    PaintPanel panel;

    Main() {
        setTitle("Paint Brush Program");
        setSize(800, 600);
        setLayout(null);

        redBtn = new JButton("Red");
        blueBtn = new JButton("Blue");
        greenBtn = new JButton("Green");
        blackBtn = new JButton("Black");
        clearBtn = new JButton("Clear");

        String widths[] = {"5", "10", "15", "20", "25"};
        widthBox = new JComboBox<>(widths);

        redBtn.setBounds(20, 20, 80, 30);
        blueBtn.setBounds(110, 20, 80, 30);
        greenBtn.setBounds(200, 20, 80, 30);
        blackBtn.setBounds(290, 20, 80, 30);
        clearBtn.setBounds(380, 20, 80, 30);
        widthBox.setBounds(480, 20, 80, 30);

        redBtn.addActionListener(this);
        blueBtn.addActionListener(this);
        greenBtn.addActionListener(this);
        blackBtn.addActionListener(this);
        clearBtn.addActionListener(this);
        widthBox.addActionListener(this);

        add(redBtn);
        add(blueBtn);
        add(greenBtn);
        add(blackBtn);
        add(clearBtn);
        add(widthBox);

        panel = new PaintPanel();
        panel.setBounds(20, 70, 740, 470);
        add(panel);

        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == redBtn) {
            panel.setCurrentColor(Color.RED);
        } else if (e.getSource() == blueBtn) {
            panel.setCurrentColor(Color.BLUE);
        } else if (e.getSource() == greenBtn) {
            panel.setCurrentColor(Color.GREEN);
        } else if (e.getSource() == blackBtn) {
            panel.setCurrentColor(Color.BLACK);
        } else if (e.getSource() == clearBtn) {
            panel.clearCanvas();
        } else if (e.getSource() == widthBox) {
            int size = Integer.parseInt((String) widthBox.getSelectedItem());
            panel.setBrushSize(size);
        }
    }

    public static void main(String[] args) {
        new Main();
    }
}

```
Output:
<img width="988" height="745" alt="image" src="https://github.com/user-attachments/assets/94929b25-f34e-481c-90e6-28386c25ba8e" />

<h2 id="program21">Program 21</h2>

```java

package mypack;

public class Add {
    public int sum(int a, int b) {
        return a + b;
    }
}
package mypack;

public class Sub {
    public int subtract(int a, int b) {
        return a - b;
    }
}
package mypack;

public class Mul {
    public int multiply(int a, int b) {
        return a * b;
    }
}
package mypack;

public class Div {
    public int divide(int a, int b) {
        return a / b;
    }
}
package mypack;

public class Square {
    public int square(int a) {
        return a * a;
    }
}

//Main Method

import mypack.*;

public class Main {
    public static void main(String[] args) {
        Add a = new Add();
        Sub s = new Sub();
        Mul m = new Mul();
        Div d = new Div();
        Square sq = new Square();

        System.out.println("Addition: " + a.sum(10, 5));
        System.out.println("Subtraction: " + s.subtract(10, 5));
        System.out.println("Multiplication: " + m.multiply(10, 5));
        System.out.println("Division: " + d.divide(10, 5));
        System.out.println("Square: " + sq.square(5));
    }
}

```
Output:
<img width="1354" height="366" alt="image" src="https://github.com/user-attachments/assets/9683e05d-dfbf-443f-913f-c7bd4c25569e" />

<h2 id="program22">Program 22</h2>

```java

package mypack;

public class Add {
    public int sum(int a, int b) {
        return a + b;
    }
}
package mypack.subpack;

public class Square {
    public int square(int a) {
        return a * a;
    }
}
import mypack.Add;
import mypack.subpack.Square;

//Main

public class Main {
    public static void main(String[] args) {

        Add a = new Add();
        Square s = new Square();

        System.out.println("Addition: " + a.sum(10, 5));
        System.out.println("Square: " + s.square(5));
    }
}

```
Output:
<img width="1918" height="983" alt="image" src="https://github.com/user-attachments/assets/ce646bae-6757-494e-83dd-9fc96846dcc2" />

<h2 id="program23">Program 23</h2>

```java

public class Main {
    public static void main(String[] args) {

        try {
            int arr[] = new int[5];

            arr[0] = 10;
            arr[1] = 20;
            arr[2] = 30;
            arr[3] = 40;
            arr[4] = 50;

            System.out.println("Accessing array elements:");
            for (int i = 0; i <= 5; i++) {  
                System.out.println("Element at index " + i + " = " + arr[i]);
            }

        } catch (ArrayIndexOutOfBoundsException e) {
            System. out.println("Array Index Out Of Bounds Exception caught!");
            System. out.println("You tried to access an invalid index in the array.");
        }

        try {
            int a = 10;
            int b = 0;

            int result = a / b;  
            System.out.println("Result = " + result);

        } catch (ArithmeticException e) {
            System. out.println("Arithmetic Exception caught!");
            System. out.println("Division by zero is not allowed.");
        }

        System.out.println("Program continues after handling exceptions.");
    }
}

```
Output:
<img width="624" height="459" alt="image" src="https://github.com/user-attachments/assets/af796bc1-0ec2-4145-aa0f-0a62667cd01b" />

<h2 id="program24">Program 24</h2>

```java

class InvalidAgeException extends Exception {
    public InvalidAgeException(String message) {
        super(message);
    }
}

public class Main {

    static void checkAge(int age) throws InvalidAgeException {
        if (age < 18 || age > 25) {
            throw new InvalidAgeException("Age must be between 18 and 25.");
        } else {
            System. out.println("Valid age. Student allowed.");
        }
    }

    public static void main(String[] args) {

        int age = 16;  

        try {
            checkAge(age);
        } catch (InvalidAgeException e) {
            System. out.println("Exception caught: " + e.getMessage());
        }

        System.out.println("Program continues...");
    }
}

```
Output:
<img width="668" height="279" alt="image" src="https://github.com/user-attachments/assets/0b07c886-4808-402b-8d37-3ab4097b34eb" />

<h2 id="program25">Program 25</h2>

```java

//Character-by-Character

import java.io.*;

public class CharFileCopy {
    public static void main(String[] args) {
        try {
            FileReader fr = new FileReader("source.txt");
            FileWriter fw = new FileWriter("dest_char.txt");

            int ch;

            while ((ch = fr.read()) != -1) {
                fw.write(ch);
            }

            fr.close();
            fw.close();

            System. out.println("File copied using character stream");
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}

//Byte-by-Byte

import java.io.*;

public class ByteFileCopy {
    public static void main(String[] args) {
        try {
            FileInputStream fis = new FileInputStream("source.txt");
            FileOutputStream fos = new FileOutputStream("dest_byte.txt");

            int b;

            while ((b = fis.read()) != -1) {
                fos.write(b);
            }

            fis.close();
            fos.close();

            System. out.println("File copied using byte stream");
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}

```
Output:
<img width="1673" height="1002" alt="image" src="https://github.com/user-attachments/assets/687ae26b-f07c-4f57-866a-74bd80266d6c" />

<h2 id="program26">Program 26</h2>

```java

interface Printer {
    void print();
}

abstract class Device {
    abstract void start();

    void stop() {
        System.out.println("Device stopped");
    }
}

class Computer extends Device implements Printer {
    void start() {
        System. out.println("Computer started");
    }

    public void print() {
        System.out.println("Printing from computer");
    }
}

public class Main {
    public static void main(String[] args) {
        Computer c = new Computer();
        c.start();
        c.print();
        c.stop();
    }
}

```
Output:
<img width="674" height="239" alt="image" src="https://github.com/user-attachments/assets/e8305388-f3b2-4001-9fc4-76b21e43a829" />

<h2 id="program27">Program 27</h2>

```java

import javax.swing.*;
import java.awt.event.*;
import java.sql.*;

public class Main extends JFrame implements ActionListener {

    JTextField t1, t2, t4, t5, t6, t7, t8, t9;
    JRadioButton r1, r2;
    ButtonGroup bg;
    JPasswordField p1;
    JButton submit, reset;

    Connection con;
    PreparedStatement pst;

    Main() {
        setTitle("Registration Form (Oracle)");
        setSize(450, 550);
        setLayout(null);

        JLabel l1 = new JLabel("Name");
        l1.setBounds(50, 30, 100, 25);

        JLabel l2 = new JLabel("Father Name");
        l2.setBounds(50, 70, 100, 25);

        JLabel l3 = new JLabel("Gender");
        l3.setBounds(50, 110, 100, 25);

        JLabel l4 = new JLabel("Age");
        l4.setBounds(50, 150, 100, 25);

        JLabel l5 = new JLabel("Address");
        l5.setBounds(50, 190, 100, 25);

        JLabel l6 = new JLabel("Email");
        l6.setBounds(50, 230, 100, 25);

        JLabel l7 = new JLabel("Mobile");
        l7.setBounds(50, 270, 100, 25);

        JLabel l8 = new JLabel("Course");
        l8.setBounds(50, 310, 100, 25);

        JLabel l9 = new JLabel("Username");
        l9.setBounds(50, 350, 100, 25);

        JLabel l10 = new JLabel("Password");
        l10.setBounds(50, 390, 100, 25);

        t1 = new JTextField();
        t1.setBounds(180, 30, 150, 25);

        t2 = new JTextField();
        t2.setBounds(180, 70, 150, 25);

        t4 = new JTextField();
        t4.setBounds(180, 150, 150, 25);

        t5 = new JTextField();
        t5.setBounds(180, 190, 150, 25);

        t6 = new JTextField();
        t6.setBounds(180, 230, 150, 25);

        t7 = new JTextField();
        t7.setBounds(180, 270, 150, 25);

        t8 = new JTextField();
        t8.setBounds(180, 310, 150, 25);

        t9 = new JTextField();
        t9.setBounds(180, 350, 150, 25);

        r1 = new JRadioButton("Male");
        r1.setBounds(180, 110, 70, 25);

        r2 = new JRadioButton("Female");
        r2.setBounds(250, 110, 80, 25);

        bg = new ButtonGroup();
        bg.add(r1);
        bg.add(r2);

        p1 = new JPasswordField();
        p1.setBounds(180, 390, 150, 25);

        submit = new JButton("Submit");
        submit.setBounds(80, 440, 100, 30);

        reset = new JButton("Reset");
        reset.setBounds(220, 440, 100, 30);

        submit.addActionListener(this);
        reset.addActionListener(this);

        add(l1);
        add(t1);
        add(l2);
        add(t2);
        add(l3);
        add(r1);
        add(r2);
        add(l4);
        add(t4);
        add(l5);
        add(t5);
        add(l6);
        add(t6);
        add(l7);
        add(t7);
        add(l8);
        add(t8);
        add(l9);
        add(t9);
        add(l10);
        add(p1);
        add(submit);
        add(reset);

        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == submit) {
            try {
                Class.forName("oracle.jdbc.OracleDriver");

                con = DriverManager.getConnection(
                        "jdbc:oracle:thin:@localhost:1521:xe",
                        "System",
                        "123");

                String gender = "";
                if (r1.isSelected()) {
                    gender = "Male";
                } else if (r2.isSelected()) {
                    gender = "Female";
                }

                String sql = "INSERT INTO registrationn VALUES (reg_seq.NEXTVAL, ?,?,?,?,?,?,?,?,?,?)";

                pst = con.prepareStatement(sql);

                pst.setString(1, t1.getText());
                pst.setString(2, t2.getText());
                pst.setString(3, gender);
                pst.setInt(4, Integer.parseInt(t4.getText()));
                pst.setString(5, t5.getText());
                pst.setString(6, t6.getText());
                pst.setString(7, t7.getText());
                pst.setString(8, t8.getText());
                pst.setString(9, t9.getText());
                pst.setString(10, new String(p1.getPassword()));

                int x = pst.executeUpdate();

                if (x > 0) {
                    JOptionPane.showMessageDialog(this, "Data Inserted Successfully!");
                } else {
                    JOptionPane.showMessageDialog(this, "Insertion Failed!");
                }

                pst.close();
                con.close();

            } catch (NumberFormatException ex) {
                JOptionPane.showMessageDialog(this, "Age must be a number");
            } catch (Exception ex) {
                JOptionPane.showMessageDialog(this, ex);
            }
        }

        if (e.getSource() == reset) {
            t1.setText("");
            t2.setText("");
            t4.setText("");
            t5.setText("");
            t6.setText("");
            t7.setText("");
            t8.setText("");
            t9.setText("");
            p1.setText("");
            bg.clearSelection();
        }
    }

    public static void main(String[] args) {
        new Main();
    }
}

```
Output:
<img width="535" height="662" alt="image" src="https://github.com/user-attachments/assets/6c1dc943-6f4b-4f6e-986c-f3949d9ff102" />




















