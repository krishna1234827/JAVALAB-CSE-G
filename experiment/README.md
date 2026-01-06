# experiment 1
## TITLE : 1a.) DISPALY PRIMITIVE DATA TYPES
```java
class DefaultPrimitiveType {
    byte primbyte;
    short primshort;
    int primint;
    double primdouble;
    char primchar;
    float primfloat;
    long primlong;
    boolean primboolean;
    public static void main(String args[]) {
        DefaultPrimitiveType dDpt = new DefaultPrimitiveType();
        System.out.println("default value of byte:" + dDpt.primbyte);
        System.out.println("default value of short:" + dDpt.primshort);
        System.out.println("default value of int:" + dDpt.primint);
        System.out.println("default value of double:" + dDpt.primdouble);
        System.out.println("default value of char:" + dDpt.primchar + " '");
        System.out.println("default value of float:" + dDpt.primfloat);
        System.out.println("default value of long:" + dDpt.primlong);
        System.out.println("default value of boolean:" + dDpt.primboolean);
    }
}
```
### Output:
![output for Default Primitvie Data Types](https://github.com/krishna1234827/JAVALAB-CSE-G/blob/8bd1538319707dc910777dc0fdb5d39b857730d8/1a_output.png)

## TITLE : 1b.) Quadratic equation solution
```java
// program code here

import java.util.Scanner;
class QuadraticEquationSolution {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a value of a:");
        double a = sc.nextDouble();
        System.out.println("Enter a value of b:");
        double b = sc.nextDouble();
        System.out.println("Enter a value of c:");
        double c = sc.nextDouble();
        double D = b * b - 4 * a * c;
        if (D > 0) {
            double x1 = (-b + Math.sqrt(D)) / (2 * a);
            double x2 = (-b - Math.sqrt(D)) / (2 * a);
            System.out.println("Roots are real and distinct:");
            System.out.println("x1 = " + x1);
            System.out.println("x2 = " + x2);
        } 
        else if (D == 0) {
            double y = -b / (2 * a);
            System.out.println("The roots are real and equal:");
            System.out.println("y = " + y);
        } 
        else {
            double real = -b / (2 * a);
            double img = Math.sqrt(-D) / (2 * a);
            System.out.println("Roots are complex:");
            System.out.println("x1 = " + real + " + " + img + "i");
            System.out.println("x2 = " + real + " - " + img + "i");
        }
        sc.close();
    }
}
```
### Output:
![output for quadratic equation](https://github.com/krishna1234827/JAVALAB-CSE-G/blob/a3c3d752727d85bd12ec1741f3fcad903cebc3ca/complex%20roots.png)
## experiment 2
## TITLE: 2a.) Implement class mechanism in java
```
class Rectangle {
   double length;
   double breadth;
   double area() {
     return length * breadth;
     }
   double perimeter() {
     return 2 * (length + breadth);
   }
 }
 class main {
   public static void main(String args[]) {
     Rectangle rect = new Rectangle();
     rect.length = 10;
     rect.breadth = 5;
     double area = rect.area();
     double perimeter = rect.perimeter();
     System.out.println("Area of given rectangle = " +area);
     System.out.println("perimeter of the given rectangle:" + perimeter);
   }
 }

```
## OUTPUT:
![output for mechanism in java](https://github.com/krishna1234827/JAVALAB-CSE-G/blob/2441d2e0e84546c71503fc99146d6909ecffdab3/2a....png)
## TITLE: 2b.) Implementing overloading methods in java
```
 class sum {
    int sum(int a,int b) {
      return a + b;
   }
   int sum(int a,int b,int c) {
      return a + b +c;
   }
   double sum(double a,double b) {
      return a + b;
   }
 }
 class main {
  public static void main(String args[]) {
    sum s = new sum();
    System.out.println("sum of 2 integers:" + s.sum(36,46));
    System.out.println("sum of 3 integers:" + s.sum(20,36,46));
    System.out.println("sum of two real number:" + s.sum(30-465,15-675));
  }
 }
```
## OUTPUT:
![output for overloading methods](https://github.com/krishna1234827/JAVALAB-CSE-G/blob/78ec70ebb16a50506829db6ca7eb84bc389f9972/2b.....png)
## TITLE :2c.) TO IMPLEMENT CUNSTRUCTOR IN JAVA
```
 class Student {
    String Sname;
    int Sage;
    double Smarks;
    Student(String name, int age, double marks) {
         Sname = name;
         Sage = age;
         Smarks = marks;
    }
    void display() {
        System.out.println(" Student Name: " + Sname);
        System.out.println(" Student Age: " + Sage);
        System.out.println(" Student Marks: " + Smarks);
    }
}
 class main {
   public static void main(String args[]) {
     Student  S = new Student("bunny",28,965);
     S.display();
   }
 }
```
## OUTPUT:
![output for constructor](https://github.com/krishna1234827/JAVALAB-CSE-G/blob/3cc2ba078e9080d6580e74fb0458b8ca6f8ab7b7/2c....png)
# Additional experiment 2
## TITLE : Fibonacis series
```
class Fibonacis {
    int firstNumber;
    int secondNumber;
    int thirdNumber;
    int sum;
    int sizeofFibsequence;
    Fibonacis(int size) {
    firstNumber = 0;
    secondNumber = 1;
    thirdNumber = 0;
    sum = 0;
    sizeofFibsequence = size;
  }
  void generateFibsequence() {
    while(sizeofFibsequence > 0) {
      if(sizeofFibsequence == 1)
    System.out.print(firstNumber + ".");
    else
       System.out.print(firstNumber + ",");
       sizeofFibsequence--;
       sum += firstNumber;
       thirdNumber = firstNumber + secondNumber;
       firstNumber = secondNumber;
       secondNumber = thirdNumber;
    }
  }
  int getFibsum() {
    if(sum > 0) {
     return sum;
    } else {
       generateFibsequence();
         return sum;
    }
  }
 }
import java.util.Scanner;
 class main {
 public static void main(String args[]) {
   System.out.print("enter the size of the sequence:");
      Scanner Sc = new Scanner(System.in);
      int size = Sc.nextInt();
      if(size > 0) {
      Fibonacis fib = new Fibonacis(size);
      System.out.println("Fibonacis series are:");
         fib.generateFibsequence();
         System.out.println("the sum of Fibonacis series:" + fib.getFibsum());
         }
         else
         System.out.println("Fibonacis sequence and cannot be calculated");
      }
 }
```
![output for Fibonacis]()



