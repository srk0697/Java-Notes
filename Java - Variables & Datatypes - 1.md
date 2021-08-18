# Computational Thinking
Computational thinking involves expressing solutions to the problems in ways that a computer can understand.
There are four major steps involved with computational thinking:

## 1. Decomposition
This involves breaking a problem into several smaller problems that are easier to understand and program. Assume that you are programming a calculator that does basic mathematical calculations. This bigger problem can be decomposed into 3 smaller sub-problems such as:

    i) Asking the user for input (user enters 4 x 6)
    ii) Computing the result (4 x 6 = 24; result = 24)
    iii) Showing the result back to the user (user gets to see 24)
    
In this way, you can solve each sub-problem separately and then later combine these solutions to solve the bigger problem of eventually making the calculator work, as expected.

Breaking down a bigger problem into smaller ones helps in simplifying the task at hand. This way, you ensure exhaustiveness in your approach and, most importantly, you get a basic framework to attack a problem. Such an approach is very important when it comes to programming. This process is known as **Decomposition**. In the next steps, we move on to start solving these problems.

### Example 1:-
**Average Ratings for a Restaurant**

You would have used an online Food-Ordering and Delivery application where you can browse through various restaurants and pick where to order food from. Assume that each restaurant displays an average of the rating given by all the customers who would have rated the restaurant in the past.

Assume that you are given a file containing all the ratings given by individual customers for a restaurant named 'SuperFood' and you need to calculate the average rating for this restaurant. How will you use the concept of decomposition to solve this problem?

Note:
Irrespective of what these ratings are and how many customers have rated the restaurant, you need to devise a generic solution. You can assume the ratings and number of customers as per your choice.

#### Answer-

let, total customer no = 5

total rating no = 5

customer 1, customer 2, customer 3 give rating = 4

customer 4 and customer 5 give rating = 4.5

so the average rating of SuperFood restaurant is = {(4*3)+(4.5*2)}/5 = 4.2
***
### Example 2:-
**Highest Rated Restaurant**

Extending the previous problem, suppose that the file given to you contains all the ratings given by individual customers for 10 different restaurants (assume that these restaurants are named as R1, R2, ..., R10). Also, remember that the entries in this list are not segregated according to the restaurants. You are required to find out the highest-rated restaurant. How will you use the concept of decomposition to solve this problem?

Note:
Irrespective of what these ratings are and how many customers have rated the restaurant, you need to devise a generic solution. You can assume the ratings and number of customers as per your choice.

#### Answer-

    let,
    total number of customers = 5
    total number of ratings = 5
    Total Restaurants number = 10
    For R1,
    assume that, customer 1, customer 2 and customer 3 give rating = 4
    customer 4 and customer 5 give rating = 4.5
    average rating = {(4*3)+(4.5*2)}/5 = 4.2
    For R2,
    assume that, customer 1 and customer 2 give rating = 4
    customer 3, customer 4 and customer 5 give the rating = 3.5
    average rating = {(4*2)+(3.5*3)}/5 = 3.7
    For R3,
    assume that, customer 1, customer 2 and customer 3 give rating = 4.5
    customer 4 and customer 5 give rating = 4.2
    average rating = {(4.5*3)+(4.2*2)}/5 = 4.38
    For R4,
    assume that, customer 1, customer 2 and customer 3 give rating = 4.5
    customer 4 and customer 5 give rating = 5
    average rating = {(4.5*3)+(5*2)}/5 = 4.7
    For R5,
    assume that, customer 1 and customer 4 give rating = 4.5
    customer 2, customer 3 and customer 5 give the rating = 3.5
    average rating = {(4.5*2)+(3.5*3)}/5 = 3.9
    For R6,
    assume that, customer 2 and customer 5 give rating = 3.5
    customer 1, customer 3 and customer 4 give the rating = 3
    average rating = {(3.5*2)+(3*3)}/5 = 3.2
    For R7,
    assume that, customer 1 give rating = 5
    customer 2, customer 3, customer 4 and customer 5 give the rating = 3.5
    average rating = {5+(3.5*4)}/5 = 3.8
    For R8,
    assume that, customer 1 give rating = 3
    customer 2, customer 3, customer 4 and customer 5 give the rating = 3.5
    average rating = {3+(3.5*4)}/5 = 3.4
    For R9,
    assume that, customer 2 and  customer 4 give rating = 4.5
    customer 1, customer 3 and customer 5 give the rating = 5
    average rating = {(4*2)+(5*3)}/5 = 4.8
    For R10,
    assume that, customer 1, customer 2, customer 3, customer 4 and customer 5 give rating = 4.5
    average rating = 4.5
    Arrange the average ratings as 
    R9>R4>R10>R3>R1>R5>R7>R2>R8>R6
    The highest-rated restaurant is R9.
***
## 2. Pattern Recognition

Let’s think of a very basic question. If you are told to find the 400th term of the sequence:

1, 3, 6, 10…. 
How will you go about it? At first, this problem may look difficult or maybe unsolvable. So you should decompose it into several more manageable sub-problems, like find the 2nd term, 3rd term, 4th term and so on till the 400th term. Let's now try to figure out how to find the 400th term.

If you look at the 2nd term, it can be either '+ 2' or 'x 3' of the 1st term. The 3rd term can be either '+ 3' or 'x 2' of 2nd term. The 4th term can be '+ 4' of 3rd term. If you observe solutions to these smaller sub-problems, then you see a pattern: 2nd term is '+ 2' of the 1st term, 3rd term is '+ 3' of the 2nd term, 4th term is '+ 4' of the 3rd term and so on.

**Pattern recognition** is the ability to recognize patterns or similarities in the smaller chunks that you break your problem down to. It is a boon if you are looking to save time and resources invested in problem-solving. It is frequently the basis for solving problems and designing problem-solving strategies. 

A real-world example can be the 'next-word suggestion' feature on your mobile keypad. Your keypad observes what you're typing. For instance, after typing a particular word, which word is used the most frequently after the typed word, and so on. Once your keypad recognizes your typing pattern, and you start typing a sentence, your keyboard is just predicting 2nd word in the sentence (based on the 1st word written by you), 3rd word in the sentence (based on the 2nd word written by you) and so on.

## 3. Abstraction

Abstraction involves working on relevant information and ignoring the information that is not useful to solve the problem at hand.

Consider the following examples:

    i) Suppose you want to buy new shoes on amazon. You just type 'https://www.amazon.in/' in the URL bar and press the Enter key. You never think of how typing this URL takes you to the amazon page, why we are writing www in URL or what is https in the beginning. Although this information is essential but is not relevant to our objective of buying shoes.

    ii) You walk easily by putting one leg after the other repeatedly without worrying about how the muscles and bones, involved, work together to accomplish this. All this internal coordination between muscles is essential, but knowing it is not relevant for your objective to walk.

    iii) Consider the same sequence we discussed earlier. How important is the fact that the numbers are even or odd in the sequence 1, 3, 6, 10…. to figuring out the 400th term? Knowing this extra information doesn't help us to solve this problem.

In all the above examples, you learned that you only need certain information to solve a problem, and it is possible that much of the available information can be irrelevant to you.

**Abstraction** means figuring out the relevant details of a problem so that it can be modelled computationally, thus reducing the complexity of the problem. In other words, it is an approach where you don’t think about a problem in very specific terms. Rather than focusing on the general information, you focus your attention on the specific key information about the problem.

## 4. Algorithm Design

Consider the task of finding the largest number in a set of random numbers. This can be done in multiple ways but you want to devise a general solution which can be applied to such similar problems in the future and also you can write it on a paper and give it to anyone who wants to solve such a problem. One such solution can be:

    i) Consider the first number as the current number as well as the current largest number.

    ii) Go to the next number on the list and treat it as the current number.

    iii) Compare the current number and the current largest number, if the current number is greater than the current largest number then our current largest number will be our current number, otherwise no need to take any action.

    iv) Follow step (ii) and step (iii) till all the numbers in the set have been compared against the current largest number.

    v) The current largest number will be the largest number in the list.

This is a representation of your plan in step-by-step sequential instructions. This is what we call algorithms or algorithm design. Remember, the steps should be well-defined, exhaustive, sequential, and should have a finite endpoint, i.e. the one who is reading the instructions should clearly know when to stop after the required result has been obtained.

Algorithmic Thinking and Algorithm Design is very important for those who want to learn to code. If you want your computer to perform a certain task for you, you have to give the instructions to it in a clear, step-by-step manner, which the computer can understand.

So you now know how to break down a larger problem into smaller ones, which are easier to solve. Then, you recognize patterns in these smaller problems, if there are any. Based on these patterns, you come up with information that is relevant to the current problem, and this helps you lay out a general framework of the problem. When you have all the information you need and you deduce the logic to be put behind solving your problem, you come up with a step-by-step solution to the problem. Let’s start learning how to give such instructions to computers so that you can use them to solve real-life problems.
___
# Introduction to Variables

The first stepping stone to computer programming is understanding what are variables. Be it in Java or any other programming language you may choose, variables play a very important role in your program. Variables are storage units in your program and facilitate a major chunk of computations that you will be doing.

**Variables** are simply containers in the computer memory to store the information you want. However, to be able to access specific information in the memory, there should be a way to uniquely identify these containers. For this purpose, we use variable names.

**Variable declaration** is the process of telling the computer that it needs to allocate certain memory to store these particular containers. We also provide names to these containers during variable declaration. Naming a variable is necessary to tell the computer to pin-point to a particular container.
___
# Variables in Java

**Syntax of Variable Declaration:**

variableType variableName; 

You first tell the computer what kind of data you will store in the variable, and then you assign a name to it. For example:

    int distance;
    int marks;
    String student1;
    String name;
 
One thing you need to keep in mind that you have to end each statement with a semi-colon (;). It tells the compiler to end one statement and start a new statement. It's same as full-stop in the English language. If you don't end a statement with a semicolon, the compiler may throw an error.

The compiler will end a statement only when it encounters a semicolon, so all the following statements are valid to declare a variable marks of type int, but you should always use the first approach.

**Syntax for Variable Initialization:**

    variableName = variableValue;

For example:

    distance = 10;

Note: Before initializing a variable, that variable must have been declared, otherwise the compiler will throw an error.

**Syntax for Variable Declaration & Initialization:**

    variableType variableName = variableValue;

For example:

    int distance = 10;
 

We can declare and initialize multiple variables in a single statement using a comma-separated list. For example

    String student1 = "Adam";
    String student2 = "Lucy";
    String student3 = "Emma";
    
This can also be done as shown below-

    String student1 = "Adam", student2 = "Lucy", student3 = "Emma";
 
We should place atleast one space between variableType and variableName, other than that there is no restriction on the number of spaces between different words in a statement. So all the following statements are valid and identical for java compiler.

### Example 1:-

You are required to initialize an integer variable using int which has the name count and assign it a value of 100.

**Test Case 1 (Sample):**

**Input:**

(There is no input for this question!)

**Output**

100

**Notes:**

  i) When you run the code, it will automatically print the value of this variable. You don't have to write the code for printing the value of this variable. It has already been written for you.
  ii) Remember that the Main class in our online IDE is named as Source class.

#### Answer-

    import java.util.*;
    public class Source {
       public static void main(String[] args) {
           int count;
           count = 100;
           System.out.println(count);
       }
    }
___
# Updating variables

As the name suggests, the values stored in these variables can change depending on the need of the program.

To update the value of a variable in Java, you follow the following format:

    <Variable Name> = <Variable Name> + <Update Value>;

For example:

    marks = marks+10;
 
You can also update the value of a variable by overriding old value with a new value. For example-

    int marks = 10;
    marks = 20;

So after the execution of the second statement, marks will store value 20.

You can also assign the value of a variable to another variable, but they should be of the same type. For example-

    int marks1 = 10;
    int marks2 = marks1;

So after the execution of the second statement, marks2 will store value 10.

For String type-

    String student1 = "Adam";
    String student2 = student1;

So after the execution of the second statement, student2 will store value "Adam". This is also the reason why we enclose String value inside double quotes, otherwise, the compiler would not have been able to tell whether the value of student2 is Adam or student1. For example-

    String name = Adam
    string s = name

So if we don't enclose values of the String variable inside double-quotes, the compiler won't be able to tell if the value of variable s is name or Adam.

You can also add another variable as the updated value. For example, consider that there is another variable called marks1 which needs to be added to marks. This would be accomplished as follows(assume all variables are int type):

    marks = marks+marks1;

So, the addition of marks and marks1 shall be assigned to the variable, marks.
___
# Working With Variables In Java

i) How to declare and initialise variables -

    int distance = 0;
    
ii) How to update variable values -


    <Variable Name> = <Variable Name> + <Update Value>
    
iii) How to print the value stored inside a variable -

    System.out.println(<Variable Name>)
    
**Braces follow the Kernighan and Ritchie style for nonempty blocks and block-like constructs:**

  i) No line break before the opening brace.

  ii) Line break after the opening brace.

  iii) Line break before the closing brace.

  iv) Line break after the closing brace, only if that brace terminates a statement or terminates the body of a method, constructor, or named class. For example, there is no line break after the brace if it is followed by else or a comma.

  v) Each time a new block or block-like construct is opened, the indent increases by two spaces. When the block ends, the indent returns to the previous indent level. The indent level applies to both the code and comments throughout the block.

![Screenshot 2021-08-18 122834](https://user-images.githubusercontent.com/88551711/129852727-36b7f393-40cb-4634-85c5-aaee5fd5f38e.png)
___
# Introduction to Data Types - I

