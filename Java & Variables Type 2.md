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
___
# Relational and Logical Operators
The boolean data type is very useful when we have to compare two quantities.

**The Relational Operators** (>, >=, <, <=, ==, !=) that are used to compare values and give an output of boolean data type, which can be stored into a boolean variable.

**The Logical Operators** “AND” , “OR” and "NOT". Logical Operators takes boolean data type as input and gives an output of boolean data type. The “AND” operation results in a true value only if both of the conditions involved are true. Whereas, the “OR” operation results in a true value even if one of the conditions involved is true.

![Markdown logo](Screenshot 2021-08-12 035747.png "Markdown")
