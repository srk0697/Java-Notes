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

# Nested If Else

Nested If Else basically means an If Else statement inside another If Else statement. You often have to check sub-conditions within existing conditions. For example, let’s say you’re going to a movie. First, you’ll check if the tickets are available at a theatre near your home. Then, you will check another condition, i.e. whether the price of the ticket is worth it. However, if the tickets aren’t available, you will not check this sub-condition.

**The syntax for nested if-else:**

     if (condition1) {
	if (condition1A) {
		Action1A;
	}
	else {
		Action1B;
	}
     }
     else {
	Action2;
     }
	
___

# Switch Case

**The syntax for switch block-**

     switch (variable) {
       case match1:
		Action1;
		break;
	
       case match2:
		Action2;
		break;
	.
	.
	.
       case matchN:
		ActionN;
		break;
	
       default:
		DefaultAction;
		break;
       }

switch-case statements help us to solve everyday life scenarios which require us to choose between different alternatives. If you don't use break statement at the end of each case block, all of the subsequent case blocks will start executing, till it executes a break statement or switch block end.
They are very similar to multiple If-Else statements, but the only difference being that Switch case statements are strictly used only when we have to only check the value of a variable and only then take an action. It is recommended to use If-Else statements in those situations where you might have to check some additional conditions besides the value of a single variable.

### Example 1:-

Can you write Java code using the switch-case statements for the coffee vending machine example you saw earlier?
A user can ask for the following drinks:

Cappuccino, code:1

Espresso,code:2

Latte,code:3

Milk,code:4

You have to take the code of the drink as input from the user and print “Preparing <name of the drink>” as output.
If the user has entered any number not within 1 to 4, then print “Drink not available”.

***Sample Input:***

1

***Sample Output:***

Preparing cappuccino

#### Answer-

	switch (code){
           case 1:
               System.out.println("Preparing cappuccino");
               break;
           case 2:
               System.out.println("Preparing espresso");
               break;
           case 3:
               System.out.println("Preparing latte");
               break;
           case 4:
               System.out.println("Preparing milk");
               break;
           default:
               System.out.println("Drink not available");
               break;
        }
***
### Example 2:-

Write Java code using Switch case statements for the following problem:

You have to create a sorting hat program. A student will be asked to enter a random number and based on that, he/she will be allotted a house. The allotment is as follows:
1-Hufflepuff 
2-Gryffindor
3-Slytherin
4-Ravenclaw
Make the default statement as “Enter a number from 1 to 4”
	
***Sample input:***
	
1
	
***Sample output:***
	
Hufflepuff

#### Answer-

    import java.util.*;
    public class Source {
    public static void main(String[] args) {

       int n;
       Scanner input= new Scanner(System.in);
       n=input.nextInt();
       switch (n){
           case 1:
               System.out.println("Hufflepuff");
               break;
           case 2:
               System.out.println("Gryffindor");
               break;
           case 3:
               System.out.println("Slytherin");
               break;
           case 4:
               System.out.println("Ravenclaw");
               break;
           default:
               System.out.println("Enter a number from 1 to 4");
        }
       }
      }
***
### Example 3:-

Write a Java program to check eligibility to drink based on entered age.(Assume legal drinking age as 21).
If the person is eligible, print “You are eligible to consume alcohol” 
If the person is not eligible, print “You are not eligible to consume alcohol. Go home kid!”
	
***Sample Input:***

21

***Sample Output:***

You are eligible to consume alcohol

#### Answer-

     import java.util.*;
     public class Source {
     public static void main(String[] args) {
	
        int age;
        Scanner input= new Scanner(System.in);
        age=input.nextInt();
        
        //write you code here
        if (age>=21){
            System.out.println("You are eligible to consume alcohol");
        }
        else {
            System.out.println("You are not eligible to consume alcohol. Go home kid!");
        }
       }
     }
### Example 4:-

Write a Java program to take the values of length and breadth from user and print whether the quadrilateral is a rectangle or a square.(You can assume that all angles in the quadrilateral are right angles).
	i) Print out “Square” in case the quadrilateral is a square
	ii) Print out “Rectangle” in case the quadrilateral is a rectangle

***Sample Input:***

4

4
***Sample Output:***

Square

#### Answer-

    import java.util.*;
    public class Source {
    public static void main(String[] args) {
	
        int length,breadth;
        Scanner input = new Scanner(System.in);
        length=input.nextInt();
        breadth=input.nextInt();
        
        //wrire your code here.
        if (length==breadth){
            System.out.println("Square");
        }
        else {
            System.out.println("Rectangle");
        }
       }
     }
***
### Example 5:-

Assume that you have built a lie detector which detects the level of chemicals X and Y.
If the sum of the amounts of X and Y is greater than 30, then the person is telling the truth.
Write Java code to take in the values of X and Y and detect whether the person is telling the truth or not.
If the person is not lying then display "The person is telling the truth.", otherwise display"The person is lying."

***Sample input:***

12

23
***Sample output:***

The person is telling the truth.

#### Answer-

    import java.util.*;
    public class Source {
    public static void main(String[] args) {
	
        int X,Y,Sum;
        Scanner input= new Scanner(System.in);
        X=input.nextInt();
        Y=input.nextInt();
        //write your code here
        Sum=(X+Y);
        if (Sum > 30){
            System.out.println("The person is telling the truth.");
        }
        else{
            System.out.println("The person is lying.");
        }
      }
    }
***
### Example 6:-

**Day of the week**

***Sample Input:***
	
January

4

***Output:***

Ohhh! It's a workday :|

#### Answer:-

        import java.util.Scanner;
        class Source {
        public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);
		// Enter month
		String month = scan.next();
		// Enter date
		int date = scan.nextInt();
		
		int day = 0;
		switch (month) {
			case "January":
				day = date;
				break;
			case "February":
				day = 31 + date;
				break;
			case "March":
				day = 31 + 28 + date;
				break;
			case "April":
				day = 31 + 28 + 31 + date;
				break;
			case "May":
				day = 31 + 28 + 31 + 30 + date;
				break;
			case "June":
				day = 31 + 28 + 31 + 30 + 31 + date;
				break;
			case "July":
				day = 31 + 28 + 31 + 30 + 31 + 30 + date;
				break;
			case "August":
				day = 31 + 28 + 31 + 30 + 31 + 30 + 31 + date;
				break;
			case "September":
				day = 31 + 28 + 31 + 30 + 31 + 30 + 31 + 31 + date;
				break;
			case "October":
				day = 31 + 28 + 31 + 30 + 31 + 30 + 31 + 31 + 30 + date;
				break;
			case "November":
				day = 31 + 28 + 31 + 30 + 31 + 30 + 31 + 31 + 30 + 31 + date;
				break;
			case "December":
				day = 31 + 28 + 31 + 30 + 31 + 30 + 31 + 31 + 30 + 31 + 30 + date;
				break;
			default:
				System.out.println("Invalid input");
		}
		int dayNumber = day % 7;
		// since day 1 is Monday
		if (dayNumber == 0 || dayNumber == 6) {
			System.out.print("Hurray!");
		} else {
			System.out.print("Ohhh! It's a work day :|");
		}
		scan.close();
            }
         }
***
### Example 7:-

Create a program for calculating the income tax to be paid by an individual earning less than 1 crore. Use conditional statements only.

![Screenshot 2021-08-16 142849](https://user-images.githubusercontent.com/88551711/129538444-c8422b1f-5341-4b40-99fb-df582f9caade.png)

**Additional information:**

	i)The basic exemption limit for individuals (i.e. below 60 years of age) is Rs. 2.50 lakhs.

	ii)The basic exemption limit for senior citizens (60 years to 80 years) is Rs. 3.00 lakhs.

	iii)The basic exemption limit for very senior citizens (80 years and above) is Rs. 5.00 lakhs.

	iv)No extra cess is to be levied.
	
**Take the income and age as inputs and return the income tax.** 

For example, if the income of an individual is 6 lacs and his/her age is < 60, then the income tax to be paid is calculated by the following set of rules:

![Screenshot 2021-08-16 155903](https://user-images.githubusercontent.com/88551711/129550163-fa07c351-5274-46b2-b70c-390a6ace0d52.png)

***Sample Input:***

600000

45

***Output:***

45000.0
									      
#### Answer-

    import java.util.Scanner;

    class Source {
    public static void main(String args[]) {
        Scanner scan = new Scanner(System.in);
        // Enter annual income
        double income = scan.nextDouble();
        // Enter age
        int age = scan.nextInt();
        
        double minimumAllowedIncome; 
        
        if ((age > 60) && (age <= 80)) {
            minimumAllowedIncome = 300000;
        } else if (age > 80) {
            minimumAllowedIncome = 500000;
        } else {
            minimumAllowedIncome = 250000;
        }
        double tax = 0.0;
        if (income > minimumAllowedIncome && income <= 500000.00) {
            tax = 0.1 * (income - minimumAllowedIncome);
        } else if (income > 500000.00 && income <= 1000000.00) {
            tax = 0.1 * (500000 - minimumAllowedIncome) + 0.2 * (income - 500000);
        } else if (income > 1000000.00) {
            tax = 0.1 * (500000 - minimumAllowedIncome) + 0.2 * (1000000 - 500000) + 0.3 * (income - 1000000);
        }
        System.out.print(tax);
        scan.close();
      }
    }
___

# Additional Reading: The Ternary Operator

The ternary operator(?:) is a conditional statement similar to the if-else statement. The format of using this operator is as follows:

**variable x = (expression) ? value if true: value if false**

***For example:***

x=(a>b)?y:z;

Here, if the condition (a>b) is true then:

	**x will be assigned the value y.**

If the given condition is not true, i.e. a<b, then:

	**x will be assigned the value z.**

Consider the following snippet of code. It checks whether the value of the variable flag is greater than 0 and assigns a value to the variable “alert” based on that.

		if (flag>0){
		   alert="ON";
		}
		else {
		   alert="OFF";
		}


This code can be written in just one line by using the ternary operator as follows:

	**alert=(flag>0)?"ON":"OFF";**

Another example can be, finding maximum value between two values. With if-else we can do something like this-

		int x, y;
		int maxValue;
		if (x > y) {
		    maxValue = x;
		}
		else {
		    maxValue = y;
		}
This code can be written in more compact form as shown below-

		int x, y;
		int maxValue = (x > y) ? x : y;

___

# Understanding loops-The While Loop

Java has constructs called loops which can facilitate repeated execution of a certain set of statements until a certain user-defined condition is met.

**The Syntax for while loop-**

	while (condition) {
	    Action;
	}


**The syntax for while loop using counter-**

	int counter = initialValue;
	while (counter < endValue) {
	    Action;
	    counter = counter + increment;
	}

**To summarise, here are the important components of any loop:**

	i) A starting point.

	ii) A loop control variable that’s also called the counter, which keeps track of how many iterations a loop has to run. The counter is incremented after each iteration.

	iii) A loop continuation condition which defines how many times a loop has to run. The condition makes sure that the loop runs until an endpoint is reached.

### Example 1:-

What will be the number of times the loop below will run?

	public static void main(String[] args) {
	   int counter=0;
	   while (counter<12){
	       counter=counter+1;
	   }
	}

#### Answer-

12, The loop will run till counter=11. But since the counter starts from zero, it will also run once when counter=0. Hence the loop will run for a total of 12 times.

### Example 2:-

Write a program that prints all the odd numbers from 25 to 1 (in decreasing order).

***Input:***
No input required

***Output*** 
25 23 21 19 17 15 13 11 9 7 5 3 1

#### Answer-

	class Source {
		public static void main(String[] args) {
		int num = 25; 
			while( num >= 1) {
		  System.out.print (num + " ");
		  num = num - 2;
		} 
	    }
	}
***
### Example 3:-

Write a program to print numbers from 1 to n, where n is a number taken as input from the user.

***Sample Input:***

4

***Sample Output:***

1

2

3

4

#### Answer-

	import java.util.*;
	public class Source {

	   public static void main(String[] args) {
	     int n;
	     Scanner input= new Scanner(System.in);
	     n=input.nextInt();
	     int counter=1;
	     while (counter<=n){
		 System.out.println(counter);
		 counter=counter+1;
	     }
	   }
	}
***
### Example 4:-

Write a program to print n multiples of x, where n and x are integers entered by the user.
The first line of input will contain x and the second line will have n.

***Sample Input:***

2

4
***Sample Output:***
2

4

6

8

#### Answer-

	import java.util.*;
	public class Source {

	   public static void main(String[] args) {
	     int x,n;
	     Scanner input= new Scanner(System.in);
	     x=input.nextInt();
	     n=input.nextInt();
	     int counter =1;
	     while (counter<=n){
		 System.out.println(x*counter);
		 counter=counter+1;
	     }
	   }
	}
***
### Example 5:-

Write a Java program to print all alphabets from a to z in lowercase.
(Hint: The ASCII value of “a” is 97)
Note: You have to print the alphabets in a single line.
***Sample Input:***

Nil

***Sample Output:***

a b c d e f g h i j k l m n o p q r s t u v w x y z

#### Answer-

	import java.util.*;
	public class Source {

	   public static void main(String[] args) {
	       int counter = 97;
	       while (counter <= 122) {
		   System.out.print((char) counter+ " ");
		   counter = counter + 1;
	       }
	   }
	}
___
# The For Loop
Let us now look at another kind of loop, the for loop.

**The syntax for for loop-**

	for (initialization condition; termination condition; increment condition) {
	    Action;
	}

**The syntax for for loop using counter-**

	for (int counter = initialValue; counter < endValue; counter += increment) {
		Action;
	}

One thing you have to keep in mind that, in for loop, we can omit any of the 3 conditions. For example, we can write for loop as shown below-

	int counter = initialValue;
	for ( ; counter < endValue; ) {
		Action;
		counterValue += increment;
	}

In the above example, we omitted both initialization and increment condition in for loop, but it is still valid. You can also write for loop as shown below-

	for ( ; ; ) {
	    Action;
	}
***
### Example 1:-
Write a code that prints the numbers between 2,000 and 3,000, which are divisible by 8 but not by 6. (Hint: apply Boolean condition - number%8==0 && number%6!=0)
				   
**Note:**
				   
Please print all the even numbers on the same line, such as:
				   
2000 2008 2024  ...
				   
and not on different lines, such as:
				   
2000
2008
2024
...

***Input:***
				   
No input required
				   
***Output:***
				   
2000 2008 2024 2032 2048 2056 2072 2080 2096 2104 2120 2128 2144 2152 2168 2176 2192 2200 2216 2224 2240 2248 2264 2272 2288 2296 2312 2320 2336 2344 2360 2368 2384 2392 2408 2416 2432 2440 2456 2464 2480 2488 2504 2512 2528 2536 2552 2560 2576 2584 2600 2608 2624 2632 2648 2656 2672 2680 2696 2704 2720 2728 2744 2752 2768 2776 2792 2800 2816 2824 2840 2848 2864 2872 2888 2896 2912 2920 2936 2944 2960 2968 2984 2992

#### Answer-

	class Source {
	  public static void main(String[] args) {
	    int i;
	    for (i = 2000; i < 3000; i++) {
	      if (i % 8 == 0 && i % 6 != 0) {
		System.out.print(i + " ");
	      }
	    }
	  }
	}
***
### Example 2:-
Write a program that prints the sum of first n numbers, where n is the input from the user. For e.g., if the user input is 10, the output of the program should be 55.
***Input: 

10

***Output:***

55

#### Answer-

	import java.util.Scanner;
	class Source {
	  public static void main(String arg[]) {
	    int sum = 0;
	    Scanner scan = new Scanner(System.in);
	    //Enter the number upto which you wish to find the sum, in the input console
	    int number = scan.nextInt();
	    for (int i = 1; i <= number; i++) {
	      sum = sum + i;
	    }
	    System.out.print(sum);
	  }
	}
***
### Example 3:-
Print first n integers starting from 0 in the reverse order using the for loop.
(n is an integer entered by the user)
				       
***Sample Input:***
				       
5
				       
***Sample Output***
				       
5
4
3
2
1
0

#### Answer-

	import java.util.*;
	public class Source {

	   public static void main(String[] args) {
	     int n;
	     Scanner input= new Scanner(System.in);
	     n=input.nextInt();
	     for (int i=n;i>=0;i--){
		 System.out.println(i);
	     }
	   }
	}
***
### Example 4:-
Take n integers as input and print their average. 
The input will be in the following format:
The first line will contain n which is the number of integers to be taken average of.
The next n lines will contain n integers.
Average of n numbers= Sum of numbers/n

***Sample Input:***
	
2
3
7

***Sample Output:***

5

#### Answer-

	import java.util.*;
	public class Source {

	   public static void main(String[] args) {

	       Scanner input= new Scanner(System.in);
	       int n=input.nextInt();
	       int sum=0,number;
	       for (int i=0;i<n;i++){
		   number=input.nextInt();
		   sum=sum+number;
	       }
	       int average=sum/n;
	       System.out.print(average);
	   }
	}
***
# Do-While loop
The syntax for do-while loop-

	do {
		Action;
	} while (condition);

The basic logic for these loops remains the same, the only difference being that the loop continuation condition is evaluated before the first iteration in case of “while” loop and after the first iteration in case of “do while”.

One use of the do-while loop can be asking the user to enter the password, and if the user enters a wrong password, we keep on asking it till he enters a right password. Here we have to ask the user for a password atleast once no matter what. We can implement this as shown below-

	int correctPIN = 123456;
	int userPIN;
	do {
		System.out.print ("Enter PIN : ");
		userPIN = scan.nextInt();
	} while (userPIN != correctPIN);
	System.out.println("Welcome");

### Example :-
Print first n integers starting from 0 in the reverse order using the do-while loop.
(n is an integer entered by the user)

***Sample Input:***

5

***Sample Output***

5
4
3
2
1
0

#### Answer-

	import java.util.*;
	public class Source {

	   public static void main(String[] args) {
	     int n;
	     Scanner input= new Scanner(System.in);
	     n=input.nextInt();
	     int counter=n;
	     do{
		 System.out.println(counter);
		 counter=counter-1;
	     }while (counter>=0);
	   }
	}
***
# Arrays: Initialization via Loops

