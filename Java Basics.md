# Syntax
When you write a code it starts with
**public static void main(String[] args)** in other words ***AS Modifier RT MN (String[] args)***.

**AS** - Access Specifier, it is used to ristrict the acces to one class to another class. Types of Access Specifier public ,private, protected, package/default.

When you want your Access Specifier to be ***public***, ***private***, ***protected*** you have to write this keywords but for ***package/default*** you don't have to write it,
program will take it automatically as a ***package/default***.
***
**Modifier** - There is two types of modifier - ***static and non-static***.

A method is static when it does not need an object to be called. When the Java program starts, the first component that is encountered is the main method, which does not have any object created. Hence, the method must be static to be called.
***
**RT/Return Type** - Whatever the method, the value is returning that will be the ***Return Type***.

If my method is returning ***String value***, my return Type will be ***String***.
If my method is returning ***int value***, my return Type will be ***int***.
If my method is returning ***nothing***, my return Type will be ***Void***.
***
**MN/Method Name** - ***main*** is the name of the method and should be kept as ***main*** only'; otherwise, the program will not run.

**String[] args** - We write ***String[] args*** in our main method to pass any arguments while interpretation.

The main method accepts a single argument: An array of elements of type String. Each string in an array is called a command-line argument. You can also write this as String...args.
***
