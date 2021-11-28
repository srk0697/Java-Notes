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
### Example 3:-

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
An array is a collection of items stored at contiguous memory locations. It store multiple items of the same type together.
An array would be created by values input by the user. The size of the array would also be dependent on the user.  It is possible to create an array using loops.

## Break Statement-
If you want to exit or terminate a loop before it's end condition is met, you can do that using break statement. We use break statement to terminate a loop when we have achieved our objective or when we realise that running loop any more will not be beneficial at all. For example, when we are searching for an element in an array, we have to look into the entire array as that element can be anywhere. But if we find that element, then there is no need to continue loop further.

	while (condition) {
		Action;

		if (objectiveAchieved) {
			break;
		}
	}
___
# Continue Statement
You learnt how to use a break statement to exit a loop. Just as in the case of a break, you don’t need to go through all the iterations when the objective is met, you may also want to skip some iterations if a condition is not met. 

The syntax for continue statement-

	while (condition) {
		if (NoNeedToPerformThisIteration) {
			continue;
		}

		Action;
	}
___
# Functions Basic
A piece of code to be re-used multiple times in a program can be written as something called a "function" and can be then reused multiple times. Consider you have a browser window open, whenever you want to open a new tab you would just click on a button without worrying how a new tab opens. Functions in Java provide you with a similar facility to do tasks without worrying about their implementation. You can also write your own functions in Java.

The length() and charAt() functions in Java which tell you the length of the string and give you a character at a particular index respectively. Let us take a look at another interesting function in Java.

Java provides you with multiple such functions which make your life easier. Also, you can write your own functions. In the next session, you will learn more about functions and how they help you in writing better computer programs.

### Example :-
Can you think of more cases where a function could be built to help you with string manipulation?

For example: Checking if two strings are equal, finding a letter in a string.

#### Answer-
There are multiple functions related to strings in Java. For example, the toUppercase() function converts all letters of a string into uppercase.
___
### Example 1:-
Write a code that prints the highest power of 2, less than or equal to a given number. For e.g., if the input number is 9, the code should print 8, as 8 or  23 is the highest power of two which is less than 9. 

***Sample Input:***

9

***Output:***

8

#### Answer-

	import java.util.Scanner;
	class Source {
	    public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		// Enter the number
		int number = scan.nextInt();
		int result = 1;
		if(number >= 2) {

		    while (result * 2 <= number) {
			result = result * 2;
		    }

		    System.out.print(result);

		} else {
		    System.out.print("Please enter an integer >= 2");
		}

		scan.close();
	    }
	  }
***
### Example 2:-
Write the programming logic in order to find the minimum element of the provided array.
(array is given in the stub)

#### Answer:-

	import java.util.Scanner;
	class Source {
	   public static void main(String[] args) {
	       int num, min;
	       int[] array = {156, 171, 260, 95, 244, 296, 137, 180, 198, 61, 70, 283, 276, 55,
	       + 100, 59, 278, 191, 109, 110, 158, 206, 77, 279, 53, 117, 217, 214, 107, 99, 222, 
	       + 275, 179, 213, 199, 139, 174, 286, 176, 155, 237, 256, 251, 187, 249, 215, 211, 113, 
	       + 144, 50, 148, 49, 170, 236, 219, 106, 71, 263, 145, 231, 190, 165, 239, 41, 177, 297,
	       + 184, 193, 287, 202, 161, 189, 79, 232, 154, 153, 208, 72, 143, 300, 233, 124, 75,
	       + 277, 63, 130, 86, 242, 203, 116, 196, 289, 146, 273, 268, 56, 104, 173, 134, 194};
	       min = array[0];

	       for (int index = 0; index < array.length; index++) {
		   if (min > array[index]) {
		       min = array[index];
		   }
	       }

	       System.out.println("Minimum value: " + min);
	   }
	}
___
# Understanding Functions
It means to operate in a particular way. For example, the function of a pencil is to write. This function is specific and clearly defined.
A function basically has a defined name and needs to be called when an action is required. When called, a function should carry out the specific task it is created for. 

Defining a function is important as it determines what the function will be able to do. When you use ‘void’ in the function definition, you cannot use the function to return a value.

![Screenshot 2021-08-22 034829](https://user-images.githubusercontent.com/88551711/130336193-30f2b438-990a-4a41-ac90-ab4f45f5bb8d.png)

When you wish to return a value, you define its data type in the function definition.

![Screenshot 2021-08-22 035009](https://user-images.githubusercontent.com/88551711/130336209-9b8de7f4-1e83-4010-8b8e-7d36a6579c4c.png)
___
# Passing Parameters
You learnt how to define functions in the last lecture. The functions you saw had a limited usage because they were not interacting with the code. They were performing an action based on predefined values. What if you want functions to be more flexible? For instance, what if you want them to perform actions based on the values input by the user. 

You just created a function that took a name input from the user and printed a greeting using the name. You can define even more parameters as required.

You must clearly define what parameters the function can take. If you define two int parameters, you can pass only two int values into it. This means that you can only pass the values that are of the same data type as the parameters defined in the function.

You should also note that the values passed into the function, while calling it, are called arguments. Thus, instead of saying you are passing values/variables into the function, you can say you are passing arguments into the function.
***
### Example 1:-
What does the function - print() do in the following code?

	public class MyClass {
	    public static void print(String var1, int var2) {
		for (int i = 0; i < var2; i++) {
		    System.out.println(var1 + " " + i);
		}
	    }

	    public static void main(String[] args) {
		String var1 = "Hello";
		int var2 = 4;
		print(var1, var2);
	    }
	}

#### Answer-

The parameters are String var1 and int var2. Due to the for loop, string var1 is printed till ‘i’ or the loop control variable, takes on the value - var2. Therefore, if var1 is ‘Hello’, and var2 is 4, the output of the function will be — “Hello 0” “Hello 1” “Hello 2” “Hello 3”
***
### Example 2:-
Write a program that takes two numbers as input and returns the square of their sum.

For e.g., if the input numbers - 4 and 9 are passsed as parameters into the function, it should return  169, which is  (4+9)2

***Sample Input:***

4

9

***Output:***

169

#### Answer-

	import java.util.Scanner;
	class Source {

	    public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		int number1 = scan.nextInt();
		int number2 = scan.nextInt();
		System.out.print(squareOfSum(number1, number2));
	    }


	    public static int squareOfSum(int x, int y){
		return (x + y) * (x + y);
	    }
	}
___
# Functions Practice
Can you use a function that can use the logic, take a number as a parameter, and return whether the number passed is a prime number or not? This way, to check if a number is a prime number, you will simply have to pass it through the function instead of writing the entire logic for it.

One of the major advantages of using functions is that if something goes wrong, you know where to make corrections that will be reflected in the entire program. Take two scenarios: one where you are checking prime numbers using the entire elaborate logic, let’s say, 10 times in different places, and you realise that you have made an error. Here, you will have to make corrections in each of these 10 places. However, if in the second scenario, you use a function, which essentially reduces the effort required, you can simply make the correction in the function body. It will be reflected in the results.

### Example 1:-
Write a function that takes two numbers as parameters and returns the LCM of these two numbers. So, if the values passed into the function are 12 and 20, the function will return the lowest common multiple of these two, i.e 60.

***Sample Input:***

12

20

***Output:***

60

#### Answer-

	import java.util.Scanner;
	class Source {

		public static void main(String[] args) {
			Scanner scan = new Scanner(System.in);
			// Enter the two numbers in the input console
			int number1 = scan.nextInt();
			int number2 = scan.nextInt();
		System.out.println(lcm(number1, number2));
		}
		public static int lcm(int number1, int number2) {
		int multiple;
			// maximum number between number1 and number2 is stored in multiple
			if (number1 > number2) {
				multiple = number1;
			} else {
				multiple = number2;
			}
		Boolean loopcontinue = true;
			// Always true
			while (loopcontinue == true) {
				if (multiple % number1 == 0 && multiple % number2 == 0) {
					break;
				}
				multiple++;
			}
	  return multiple;
	  }
	}
___
# Pass by Value
Java uses ‘pass by value’, i.e. the values are copied into the parameters of the function, and the function performs its action based on these copied values, leaving the main variables untouched.

Now you may be wondering how to use functions to modify the variables. You can achieve the desired results by returning the modified values using a function, storing them in a temporary variable and then reassigning them to the concerned variables.

There is another mechanism called ‘pass by reference’ in some programming languages, using which, variables can be modified using functions. Although Java doesn’t support pass by reference, you will learn to achieve the desired results in further modules.

### Example 1:-
Consider a scenario where your friend wants you to create a function that takes a string as input and then replaces the string with the upper case version.

	public class StringUpperCase {
	    public static void main(String[] args) {
		String string1 = "Welcome";
		uppercase(string1);
		System.out.println(string1);
	    }

	    public static String uppercase(String string1) {
		string1.toUpperCase();
		return string1;
	    }
	}

What will be the output of the code above?

#### Answer-

**Welcome**

Function toUpperCase() creates a new String based on the variable value it was called upon, it doesn't change the variable itself. For example -

	String str = "hello";
	String up = str.toUpperCase();

	System.out.println (str);
	System.out.println (up);

The output of the above code will be -

	hello
	HELLO

As we are neither storing String returned by toUpperCase() function nor we are returning it, the changes will not get reflected.
___
# Inbuilt Functions

### Question 1:-
List down all the inbuilt functions you have used till now.

#### Answer-
System.out.println()
System.out.print()
scanner.nextInt()
scanner.nextFloat()
scanner.next()
scanner.nextLine()
string.length()
string.toUpperCase()
.
.
.
***
### Question 2:-
**MATH Library**

For the following question, please look through Javadoc's documentation for the Math class.

https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html

Which Math method will return the value of ‘a’ raised to the power ‘b’?

#### Answer-

Math.pow(a, b)

Function pow(a,b) returns a^b.
***
### Example 1:-
You are given an array of decimal numbers. You are required to round these into integers. Read the documentation below, and use the function that fits best to write the code.

https://docs.oracle.com/javase/7/docs/api/java/lang/Math.html

***Input:***

No input required

***Output:***

10.0 20.0 31.0 41.0 50.0 60.0 72.0

#### Answer-

	class Source {
	   public static void main(String[] args) { 
	       double[] array = {10.32,20.36,30.50,40.51,50.49,60.43,71.71};

	       for(int i = 0; i <  array.length; i++) {
		   array[i]= Math.round(array[i]);
	       }


	       for(int i = 0; i <  array.length; i++) {
		   System.out.print(array[i] + " ");
	       }

	   }
	}
***
### Example 2:-
There is an internal library called Arrays, which can perform multiple operations on arrays.

https://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html

Find the function that can sort an array, and use it to sort the array given in the question. 

(**Hint**: Use the internal library sort() to sort a given array. For e.g., ***sort(long[] a)*** sorts the specified array in ascending numerical order.) 

***Input:***

No Input Required

***Output:***

2 12 19 29 34 43 45 56

#### Answer-

	import java.util.Arrays;
	class Source {
	  public static void main(String[] args) {
	    int[] array = {29,34,12,45,56,02,43, 19};
	    Arrays.sort(array);
	    for(int i=0; i<array.length; i++) {
	      System.out.print(array[i] + " ");
	    }
	  }
	}
___
# Reading from a File
Till now, you created programs that take inputs from users. But what if you want to read a text or numbers from a file on your computer? You can use some internal libraries in Java to read from files. 

***We can read a file line-by-line as shown below-***

![Screenshot 2021-08-22 183829](https://user-images.githubusercontent.com/88551711/130356455-36b59a21-c158-4e10-96f8-3490b6e13fad.png)

***We can read a file word-by-word as shown below-***

![Screenshot 2021-08-22 184040](https://user-images.githubusercontent.com/88551711/130356507-3885bdfe-2827-4832-b45d-72d5e7acfd62.png)
___
# Exceptions
While writing your programs, you would have encountered many errors. It is indeed very irritating to encounter such errors. If a user is using your program and encounters such errors, he/she may lose trust in it. 

Let’s say you were loading a website page. The page didn’t load, but you got a simple message saying “Page not found”. Although there was an error, the website program was able to identify the error, mask the original error message, and send out a simple readable message — “Page not found”. But what if you got the entire technical message? You would lose trust in the creators of the website. Thus, you have to handle errors in a program.

**Note:** In JAVA, when you try to divide a variable of ***int*** data type by 0, Java throws an ***Arithmetic Exception***. However, when you try to divide a variable of ***float or double*** data type by 0, it returns ***Infinity*** instead of an exception.

![Screenshot 2021-08-22 192532](https://user-images.githubusercontent.com/88551711/130357788-ece08cf7-6a77-44d6-9017-02047582db20.png)

**Above code when run throws "ArithmeticException".**

![Screenshot 2021-08-22 192653](https://user-images.githubusercontent.com/88551711/130357828-0a504689-cfc6-4d33-84c0-3e8b6abd9038.png)

**Above code when run gives "Infinity" as output.**

You learnt how you can handle exceptions using the try and catch blocks. Here’s how a Try and Catch block looks:

![Screenshot 2021-08-22 192815](https://user-images.githubusercontent.com/88551711/130357869-5b616bfa-7607-4a04-b788-a9ca4eb50e1d.png)

The try block contains the code where exceptions may arise. If an exception occurs, it is caught by the catch block, and the statement inside the block is executed. 

A **compile-time error** is any type of error that prevents a java program from compiling, e.g. syntax error, incorrect data-types etc. Checked exceptions cause compile-time errors if left unhandled.

A **runtime error**, on the other hand, arises while the program is running. This could happen due to unexpected user input or an incorrect logic etc.

So, now you know why you used **“throws FileNotFoundException”** when you were writing the code to read text from an external file. The **throws** keyword specifies that an exception may arise in a particular method. It is different from try and catch in that it has no provision to handle the exception and thus, it can’t catch the error and execute the corresponding action, e.g. displaying a different simplified message to the user.

You learnt about the various kinds of exceptions that may arise in your codes. You learnt about checked and unchecked exceptions. Checked exceptions are those that are checked while a program is being compiled. A program will not compile if there is no provision to handle these exceptions in your code. On the other hand, for unchecked exceptions, the program may compile even if there is no provision to handle them.
***
### Example :-
The following code throws a compilation error when executed. How would you handle the error? 

Change the code so that it is compiled without an error. (**Hint:** A statement in the code throws a checked exception.)

***Sample Input:***

Hello

***Output:***

You wrote: Hello

#### Answer-

	import java.io.BufferedReader;
	import java.io.IOException;
	import java.io.InputStreamReader;

	class Source {
	   public static void main(String[] args) {
	       System.out.print("Write :");
	       BufferedReader stdin = new BufferedReader(new InputStreamReader(System.in));

	       try {
		   String inData;
		   inData = stdin.readLine();

		   System.out.print("You wrote :" + inData);
	       } catch (Exception e) {
		 System.out.print(e);
	       }
	   }
	}
___
# Writing to a File
You already learnt how to read from a file. You will now learn how to write the output of your code to a file.

![Screenshot 2021-08-22 194914](https://user-images.githubusercontent.com/88551711/130358477-3c4cc9a0-5eda-4bde-b32d-60db0c8b7bda.png)

**We can write to a file as shown above-**

This will make sure that you have your results in a saved format for comparison or in situations when you need to present the output of your code to your clients.
___
### Question 1:-

**Functions**

What are the return type and the expected parameter for the following function?

	public static String getLoginUrl(String redirectPage) {
		User user = userService.getCurrentUser();

		if (user == null) {
		    return userService.createLoginURL(redirectPage);
		}
		return redirectPage;
	    }

#### Answer-

**Return type: String & Expected parameter: String redirectPage**

The return type of the function is String as is defined in “public String … “. It takes the parameter ‘String redirectPage’.
***
### Question 2:-

**Identify the Bug**

You are given a program that contains the printBackwards function, which is supposed to print out an array of integers backwards.

To be specific, if there is an int array of [1,2,3,4,5], the printBackwards function should print out: 5 4 3 2 1.

However, there is a bug in the code, and the function is not working as expected. 

	public void printBackwards(int[] numbers) {
	    for(int i=numbers.length-1; i > 0; i--) {
		System.out.println(numbers[i]);
	    }
	}

#### Answer-

The for loop stops running when i is equal to 1. Therefore, you will never print the 0th index element of the numbers array. For it to work as expected, it should be written as shown below -

	public void printBackwards(int[] numbers) {
	    for(int i=numbers.length-1; i >= 0; i--) {
		System.out.println(numbers[i]);
	    }
	}
***
# Question 3:-
Imagine you are building a Facebook clone.
Write a function called ‘mostVotes’ that —
 1) takes in an int array called votesPerUser as a parameter, where each element in the array represents the number of votes received by the user, with the userId at that index.

 2) returns the index of the user with the most votes.

 3) if there are ties between users with the most votes, returns the index of the first user with the most votes. For example, if the 0th and 7th users in the array both have 20     votes, and both have the most number of votes, they return 0. 

For example, if the array is - 2 4 3 5 6 3

Output would be - User with the most votes is User: 4

An array has already been initialized in the code below. So, you don't have to give any input.

***Input:***

No input required

***Output:***

User with the most votes is User: 2

#### Answer:-

	class Source {
	  public static void main(String args[]) {
	    int[] votes = {1,2,34,5,6,7,8,9,10,11,12,13,14,15};
	    int userWithMostVotes = mostVotes(votes); 
	    System.out.println("User with the most votes is User: " + userWithMostVotes);  
	  }

	  public static int mostVotes(int[] votesPerUser) {
	    int userWithMostVotes = 0; 

	    for(int i=0; i < votesPerUser.length; i++) {
	      if(votesPerUser[i] > votesPerUser[userWithMostVotes]) {
		userWithMostVotes = i;
	      }
	    }
	    return userWithMostVotes;
	  }
	}
___
