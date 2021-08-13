# Conditional Statements and If Else

The syntax for an if-else statement-

    if (condition == true) {
       Perform Action 1;
    }
    else {
        Perform Action 2;
    }
   
Usually in situations in which there are two choices, and only one of those choices need to be executed at any given point of time If Else Statements are used. One of the condition is mentioned inside the If block, and the other condition is mentioned inside the Else block.
The general points to keep in mind are:-

 1. If Else statements are used in those cases where only one out of the two code blocks needs to be executed at any given point of time.

 2.One of the condition and action is mentioned in the If block

 3.The other condition and action are mentioned in the Else block.
 
 ![Screenshot 2021-08-14 015351](https://user-images.githubusercontent.com/88551711/129420621-1c796f42-845e-4368-a569-f9a06bba9aea.png)
 
 ### Example :-
 
 Write a Java program to determine if a number entered by the user is odd or even.(Assume that the user will enter a positive integer only).
  (i) Print out "the number entered is even" if the number entered is even
  (ii) Print out "the number entered is odd" if the entered number if odd

***Sample Input:***
2
***Sample Output:***
The number entered is even

#### Answer-

    import java.util.*;
    public class Source {
    public static void main(String[] args) {
    int n;
    Scanner input= new Scanner(System.in);
    n=input.nextInt();
    if (n%2==0){
        System.out.println("The number entered is even");
    }
    else {
        System.out.println("The number entered is odd");
      }
     }
    }
___

# Else If Statements

**Syntex for else-if statement-**

    if (condition1 == true) {
	  Action1;
    }
     else if (condition2 == true) {
	   Action2;
    }
     else if (condition3 == true) {
	   Action3;
    }
    .
    .
    .
     else if (conditionN == true) {
	   ActionN;
    }
     else {
	   Else Action;
    }

In situations where there might be several possible alternatives and only one of those alternatives need to be executed at any given point of time, we can use else-if statements, wherein each alternative is mentioned within one else if block.

### Example 1:-

Write Java code to check whether numbers entered by the user are in increasing order or decreasing and print “The numbers entered are in increasing order” for increasing order and “The numbers entered are in decreasing order” for decreasing order.
If the numbers are in neither increasing order then print “The number are in neither in increasing order nor in decreasing order”.
***Sample Input:***
11
19
132
***Sample Output:***
The numbers entered are in increasing order

#### Answer-

    import java.util.*;
    public class Source {

     public static void main(String[] args) {

       int n1, n2, n3;
       Scanner input = new Scanner(System.in);
       n1 = input.nextInt();
       n2 = input.nextInt();
       n3 = input.nextInt();
       
       if (n1<n2 && n2<n3){
           System.out.println("The numbers entered are in increasing order");
       }
       else if (n1>n2 && n2>n3){
           System.out.println("The numbers entered are in decreasing order");
       }
       else {
           System.out.println("The number are in neither in increasing order nor in decreasing order");
       }
     }
    }
***
#### Example 2:-

Write a Java program to print a student’s grade based on his marks. You will take the student’s name and marks as input and determine the grade based on the following:


***Marks | Grade
>100 | A
>80 & <=100 | B
>60 & <=80 | C
>40 & <=60 | D
<=40 | E

***Input format:*** 
The first line will contain the name of the student and the second line will contain student's marks.
Output format:
The program should print:
The grade scored by <name> is <grade>.

***Sample Input:***
Aishwarya
33
***Sample Output:***
The grade scored by Aishwarya is E

***Sample Input:***
Aishwarya
49
Sample Output:
The grade scored by Aishwarya is D
  
#### Answer-
  
     import java.util.*;
     public class Source {

     public static void main(String[] args) {

       String name;
       int marks;
       Scanner input = new Scanner(System.in);
       name = input.nextLine();
       marks = input.nextInt();
       if (marks > 100) {
           System.out.println("The grade scored by " + name+" is A");
       }
       else if (marks<=100 && marks>80){
           System.out.println("The grade scored by " + name+" is B");

       }
       else if (marks<=80 && marks>60){
           System.out.println("The grade scored by " + name+" is C");
       }
       else if (marks<=60 && marks>40){
           System.out.println("The grade scored by " + name+" is D");
       }
       else if (marks<=40){
           System.out.println("The grade scored by " + name+" is E");
       }
      }
     }

***
### Example :-

**Lie Detector** 

You will be taking chemicals X,Y, A and B as inputs. Also, you will take the heart rate(heartRate) as input.

The person is telling the truth if one of the following conditions are met:

Sum of amounts of X and Y is greater than 30
Either A is greater than 3 or B is less than 6
Heart rate is equal to 70 and X is greater than 3


The first four lines of input will have X,Y,A and B as inputs in that particular order.

The next line of input will have the heart rate.

***Sample input:***

12

23

1

3

77

***Sample output:***

The person is telling the truth.

***Sample input:***

1

2

1

7

77

***Output:***

The person is lying

#### Answer-

     import java.util.*;
     public class Source {

     public static void main(String[] args) {

       int X,Y,A,B,heartRate;
       Scanner input= new Scanner(System.in);
       X=input.nextInt();
       Y=input.nextInt();
       A=input.nextInt();
       B=input.nextInt();
       heartRate=input.nextInt();
       if (X+Y>30){
           System.out.println("The person is telling the truth.");
       }
       else if (A>3 || B<6){

           System.out.println("The person is telling the truth.");
       }
       else if (heartRate==70 && X>3){
           System.out.println("The person is telling the truth.");
       }
       else {
           System.out.println("The person is lying");
       }
      }
     }

___

#
