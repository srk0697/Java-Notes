# Arithmetic Operators - I
In Java, +, -, and * are the symbols used for addition, subtraction, and multiplication respectively. 
For division, the “/” symbol is used.

**The syntax for addition, subtraction, multiplication and division are shown below.**

    int x = 7;
    int y = 4;
    int a = x + y; //a = 11
    int s = x - y; //s = 3
    int m = x * y; //m = 28
    int d = x / y; //d = 1
    double dd = x / y; //dd = 1.0

'//' symbol is used to write comments in java. Anything after '//' in a line is ignored by the compiler.
Also, in the case of multiple calculations, the general **BODMAS rule** is followed. Remember, to prioritise something, you use parentheses.

***A few important takeaways:***
i) Dividing two integers will always give back an integer. So dividing 5 by 4 will give you 1 and not 1.25. The portion after the decimal is ignored.

ii) Similarly, dividing two doubles always gives back a double. So dividing 4 stored in a double variable by 2 stored in a double variable will give back a double, 2.0 and not an int, 2.
___
# Arithmetic Operations - II
The mod operator is used to store the remainder of the division between two numbers. It is very useful in cases such as trying to find an odd number or checking divisibility.

### Example 1:-
What will the output of the following code be? Write your answer in the box below.

    int a = 5;

    int b = 4;

    int c = 3;

    double z = (a + b - c) / a * b;

    System.out.println(z);

#### Answer-
4
***
### Example 2:-
Let’s say you have a 5-digit number, 23456. You are supposed to write a code that prints numbers in the ones, tens, hundreds, thousands, and ten thousands places of this number. In the text box below, write the steps you will follow to write the code. Share it on the discussion forum. Here, you only need to write the approach in a step-by-step manner, just like you did with algorithm design in the case of computational thinking.
#### Answer-
    public class arithematic {
    public static void main(String[] args)
    {
       int number = 23456;

       //for ten thousands place divide the number by 10000
        int tenThousandsPlace = number/10000;
        System.out.println(tenThousandsPlace);

        //for thousands place divide the number by 1000
        int x = number/1000;
        int thousandsPlace = x-(tenThousandsPlace*10);
        System.out.println(thousandsPlace);

        //for hundreds place divide the number by 100
        int y = number/100;
        int hundredsPlace = y - ((tenThousandsPlace*100) + (thousandsPlace*10));
        System.out.println(hundredsPlace);

        //for tens place divide the number by 10
        int z = number/10;
        int tensPlace = z- ((tenThousandsPlace*1000) + (thousandsPlace*100) +       (hundredsPlace*10));
        System.out.println(tensPlace);

        //for units place
        int unitsPlace = number- ((tenThousandsPlace*10000) + (thousandsPlace*1000) + (hundredsPlace*100) +(tensPlace*10));
        System.out.println(unitsPlace);
     }
    }
___
# User Input
Explanation of the Scanner Code

**First, you wrote the following statement to be able to use the Scanner class:**

    Scanner input= new Scanner(System.in);


**Here, “input” is the name of your Scanner. You can name the Scanner absolutely anything(like choosing variable names).**

This statement “new Scanner(System.in)” prompts Java to provide you with a new Scanner to “scan” the input given by users.

You can then use the following statement to read some integer data given as input from the user:

    a=input.nextInt();

Here, the “.nextInt()” keywords tell you scanner(named “input”) to look for the next data entered by the user and store it in the variable “a”.

Remember, for Java to know where should it get the code for the Scanner from, you have to add the following statement at the top of your code file:

    import java.util.Scanner;

### Example 1:-
Write Java code below which  —

   i) Asks the user to input three integer variables: a, b, and c

   ii) Does the following calculation: a*b+c

   iii) Prints out the value obtained in step 2

***Input***

a = 2, b = 3, c = 4 

***Output***

10

#### Answer-

    import java.util.Scanner;
    public class Source {
    public static void main( String[] args) {
   
    int a;
    int b;
    int c;

    Scanner input = new Scanner(System.in);
    
    a= input.nextInt();
    b= input.nextInt();
    c= input.nextInt();
    System.out.println(a*b+c);
    }
    }
___
# Casting
If you want to store a double value to an int data type, you can do it by casting, which otherwise throws an error.

    double d = 2.2;
    int i = (int) d;
 
Please note that here d is treated as int data type just for this assignment operation. The variable d remains of the type double only; i.e. if you use d somewhere else, it will behave as a double. Hence this is just a temporary conversion to an int.

### Example 1:-
The following variables have been initialized for you:
   int a;
   float f;
   double d;
You have to cast the variable into different data types as follows:
   i) Cast a as float to a variable x.
   ii) Cast f as an integer to a variable y.
   iii) Cast d as float to a variable z.
Hint: You have to initialize the variables x,y and z of proper data types.

Note: The required code to take user input is already written for you. Similar to nextInt(), nextFloat() is used to take floating point data as input and nextDouble() takes a double value as input.

***Sample Input:*** 
11
12.2345
12.34567895343534611
***Sample Output:***
x=11.0 y=12 z=12.345679

#### Answer-

    import java.util.*;
    public class Source {
    public static void main(String[] args) {

       Scanner input= new Scanner(System.in);
       int a=input.nextInt();
       float f=input.nextFloat();
       double d=input.nextDouble();
       float x;
       int y;
       float z;
       x=(float)a;
       y=(int)f;
       z=(float)d;
       System.out.println("x="+x+" y="+y+" z="+z);

     }
    }
***
### Example 2:-
Write a Java program to take the temperature from the user in Celsius, convert it into fahrenheit and display it to the user. You can use the following formula for this purpose:
F=9C/5+32
Where, C is the temperature in celsius and F is the temperature in fahrenheit.

**Note: C will be entered in integer form but F can be a float.

***Sample Input:*** 1
***Sample Output:*** 33.8

#### Answer-

    import java.util.*;
    public class Source {

    public static void main(String[] args) {

      int C;
      float F;
      Scanner input= new Scanner(System.in);
      C=input.nextInt();
      F=9*(float)C/5+32;
      System.out.println(F);
     }
    }
___
# String And Charecters
“char” data type is used to store single characters like ‘a’, ‘$’ or ‘1’.
 
To initialise and declare a string variable by using the keyword ‘String’. All the values of this data type should be enclosed within double-quotes.
Also, string concatenation, which is the combining of two or more strings to create one single string. Here, empty double quotes or spaces within quotes are used to ensure proper spacing in the final string. Eg. The concatenation of "Ankit" and "Garg" to print "Ankit Garg" can be done by writing “Ankit” + “ ” + “Garg”.

### Example:-

    class Main {

    public static void main(String[] args) {
  
    String firstName = "John";
   
    String lastName = "Lennon";
   
    String fullName = firstName+" "+lastName;
   
    System.out.println("My name is "+fullName);
   
      }
    }
#### Output:
My name is John Lennon.
___
# Arrays
Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

Note that all the elements in an array can only be of one data type. i.e if an array is declared as String, only string type data can be stored at each index and no other data type is compatible.

You can declare an array variable of String data type in two ways-

1. String student[];
 

2. String[] student;
 

Both these statements are valid and identical for a compiler.
***
Once you have declared an array, you can initialize that array as shown below-

 **students = new String[4];**
***
While initializing, you also specify how many elements will be stored in that array. You can declare and initialize an array in the same line as shown below-

 (i).  String students[] = new String[4];
 

 (ii). String[] students = new String[4];
 ***
Each element in an array can be accessed using its index. **The index starts from 0 and not 1**. We can access an element of an array as shown below-

**students[0] = "Adam";**

**students[1] = "Lucy";**

**System.out.println( students[0] );**

**System.out.println( students[1] );**

### Example 1:-

In which of the following cases would you NOT use an array to store the data?(consider that marks and nutritional intake are to be stored as integer values whereas names are to be stored as strings.)

#### Answer

Marks and Names of students in a class. Marks are of int data type whereas names are of the String data type and hence cannot be stored in the same array. An array can store elements only of the same data type.
***
There is another way to declare and initialize an array in the same line.

**String[] students = {"Adam", "Lucy", "Emma", "John"};**

***
### Example 2:-

    class Main {

    public static void main(String[] args) {
  
    String students[];
    
    String names[] = {"Adam","Lucy","Emma","John"}; System.out.println(names[3]);
    
       }
    }

### Output:

John

### Example 3:-

Write a Java program to take the marks of students from roll numbers 0 to 4 and store them in an array. After storing the marks, print the marks of the student with roll number 4.

***Sample Input:***
10
11
12
13
14
***Sample Output:***
14

#### Answer

     import java.util.*;
     public class Source {
     public static void main(String[] args) {

      int marks[];
      marks= new int[5];
      Scanner input= new Scanner(System.in);
      marks[0]=input.nextInt();
      marks[1]=input.nextInt();
      marks[2]=input.nextInt();
      marks[3]=input.nextInt();
      marks[4]=input.nextInt();
      System.out.println(marks[4]);
      }
    }

### Example 4:-

In addition to taking marks as input, write code to take as input a student’s roll number and display his/her marks.
Here, roll numbers start from 0.
The first 5 lines will contain marks of students and the sixth line will contain roll number of the student whose marks are to be displayed.
Note: The following statement will print the marks of a student whose roll number is stored in the variable rollNumber :
System.out.println(marks[rollNumber]);
***Sample Input:***
11
12
13
14
15
3

***Sample Output:***
The student with roll number 3 has scored 14 marks

#### Answer

    import java.util.*;
    public class Source {  
    public static void main(String[] args) {

      int marks[];
      marks= new int[5];
      Scanner input= new Scanner(System.in);
      marks[0]=input.nextInt();
      marks[1]=input.nextInt();
      marks[2]=input.nextInt();
      marks[3]=input.nextInt();
      marks[4]=input.nextInt();
      
      int rollNumber;
      rollNumber=input.nextInt();
      System.out.println("The student with roll number "+rollNumber+" has scored "+marks[rollNumber]+" marks");
      }
    }
___
# Relational and Logical Operators
The boolean data type is very useful when we have to compare two quantities.

**The Relational Operators** (>, >=, <, <=, ==, !=) that are used to compare values and give an output of boolean data type, which can be stored into a boolean variable.

**The Logical Operators** “AND” , “OR” and "NOT". Logical Operators takes boolean data type as input and gives an output of boolean data type. The “AND” operation results in a true value only if both of the conditions involved are true. Whereas, the “OR” operation results in a true value even if one of the conditions involved is true.

![Screenshot 2021-08-12 035747](https://user-images.githubusercontent.com/88551711/129225482-7bedf7a9-206f-458b-a610-944604397bc9.png)

![Screenshot 2021-08-12 035829](https://user-images.githubusercontent.com/88551711/129228305-0a5e49c9-95e0-4e49-892a-9cec0c2a8d0a.png)

![Screenshot 2021-08-12 042750](https://user-images.githubusercontent.com/88551711/129228343-512e67fc-71bc-4c85-afea-a9ce7a4b51c7.png)

___

# Precendence Order of Logical Operators

Just like arithmetic operations follow the BODMAS rule, similarly, there is a predefined precedence order in which a statement with logical operators is evaluated.

### Example 1:-

Consider that there are four buttons operating the same bulb, namely switch A, B, C and D.

The bulb will be on only if at least one of the following conditions is true:

(i) A, B, C and D all are switched on.

(ii) A and B are switched on or D and C are switched on.

Consider that A, B, C and D all are boolean variables. The 'on' state of the switch represents ‘true’ and the off state represents ‘false’. Write the statement using logical operators to represent the state of the bulb.

(i.e. the statement will evaluate to true if the bulb is switched on)

#### Answer

Consider all situations when the bulb is switched on:

(i) Since all the boolean variables have to be true, we will use the “&&” operator here as follows to represent this situation: A && B && C && D

(ii) When A and B are switched on “(A && B)” will evaluate to true. Whereas when D and C are on “(D && C)” will evaluate to true. Since only one of these has to be true, this situation will be represented as follows: (A && B) || (D && C)

For the bulb to be switched on, only one of these conditions has to be true.

Hence, the required logical statement is:

(A && B && C && D) || ((A && B) || (D && C))

### Example 2:-

Assume that you have built a lie detector which detects the level of chemicals X and Y.

If the sum of the amounts of X and Y is greater than 30, then the person is telling the truth.

Write Java code to take in the values of X and Y and detect whether the person is telling the truth or not. If the person is telling the truth, display "The statement said by the person is true". If the person is lying then display "The statement said by the person is false".

***Sample input:***

12

23

***Sample output:***

The statement said by the person is true

#### Answer

    import java.util.*;
    public class Source {
    public static void main(String[] args) {

      int X,Y;
      Scanner input= new Scanner(System.in);
      X=input.nextInt();
      Y=input.nextInt();
      boolean test;
      test=(X+Y)>30;
      System.out.println("The statement said by the person is "+test);
      }
    }

___

# Errors and Debugging

A run-time error will only occur when the code is actually running. These errors are the most difficult as they lead to unexpected program crashes and bugs in your code, both of which can be hard to track down and fix.

However, syntax errors are compile-time errors. Compile-time errors occur when codes are written in ways in which the Java compiler does not recognise. The compiler will display errors to alert you about something that will not compile and, therefore, cannot be run.

___

# EXAMPLES:-

### Question 1:-

Write a code below that takes a 5-digit positive number from the user as an input.
For example, you can take 34768 as an input. The program should print the numbers in the ones, tens, hundreds, thousands, and ten thousands places of the 5-digit number the user inputs.

***Input:*** 
34768

***Output:***
3
4
7
6
8

#### Answer-

    import java.util.Scanner;
    class Source {

     public static void main(String[] args) {


        //Create new scanner
        Scanner input = new Scanner(System.in);

        //Values of each digit
        int tenThousands, thousands, hundreds, tens, ones;

        //Prompt user to input 5 digit number
        
        int number = input.nextInt();
        if (number > 99999) {
            System.out.println("Error! Number more than 5 digits.");
        }
        else if (number < 10000) {
            System.out.println("Error! Number less than 5 digits.");
        }
        else if (10000<=number&&number<=99999){

            //Displays ten thousands place digit
            tenThousands = number / 10000;
            System.out.println(tenThousands);

            //Displays thousands digit
            thousands = (number % 10000) / 1000;
            System.out.println(thousands);

            //Displays hundreds place digit
            hundreds = number % 1000 / 100;
            System.out.println(hundreds);

            //Displays tens digit
            tens = (number % 100) / 10;
            System.out.println(tens);

            //Displays ones digit
            ones = number % 10;
            System.out.println(ones);


            //Error if number is less or more than five digits
        }

      }
    }
***    
### Question 2:-

Let’s say you have two variables, a and b:

a is an int variable initialised to 6 and
b is a double variable initialised to 5.5 

Now you want to add these two variables and print their sum, but you’re not interested in the decimal part of a + b.

Write a code that computes a + b and prints out only the whole number part of the result.

***Input:***
No input required

***Output:***
11

#### Answer-

    class Source {
    public static void main(String[] args) {
       int a = 6;
       double b = 5.5;
       int sum = a + (int)b;
       System.out.println(sum);
      }
     }
***
### Question 3:-

Write a program that does the following:

1.It creates a String array called "names", and the array is initialised with a size of four. In other words, create a String array called "names" that can store four entries.
2.It stores the first names ‘Henry’ and ‘Shane’ in the first two entries.
3.It stores the last names ‘Sharma’ and ‘Watson’ in the next two entries.
4.It prints out, on separate lines, the first name + last name of the two names stored in the names array, e.g.

#### Answer-

    class Source {
    public static void main(String[] args) {
    String employeeNames[] = {"Henry", "Shane", "Sharma", "Watson"};

    System.out.println(employeeNames[0] + " " + employeeNames[2]);
    System.out.println(employeeNames[1] + " " + employeeNames[3]);
     }
    }
***
### Question 4:-

Let’s say someone is booking an air ticket for himself and his brother. There is an offer that says that he will get a 20% discount if both he and his brother are less than 25 years old.
Write a code that prints ‘True’ if he is eligible for the offer and ‘False’ if he is not eligible.

Specifically, the program should —

(i) Ask the user to enter his age
(ii) Ask the user to enter the age of his brother
(iii) Store the ages of the user and the user’s brother
(iv) Print "true" if the user is eligible for the discount or "false" if the user is not eligible for the discount  
(v) Please note that age has to be non- negative. 
(vi) So, in case the user enters the age which is less than or equal to 0, the program should return false.

Input:
25,28

Output:
false

Hint: Do you remember the Scanner class we talked about, which helped you take inputs from the user? If you do, then use a boolean variable that stores this condition and returns true or false.

#### Answer-

    import java.util.Scanner;
    class Source {
    public static void main(String[] args) {
       int myAge;
       int ageOfBrother;
       Scanner input = new Scanner(System.in);
       myAge = input.nextInt();
       ageOfBrother = input.nextInt();
       boolean discount = (myAge < 25 && ageOfBrother < 25 && myAge > 0 && ageOfBrother>0);
       System.out.println(discount);
      }
    }
