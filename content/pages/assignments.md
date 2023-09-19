---
content_type: page
description: This section provides the assignments of the course along with supporting
  files.
learning_resource_types:
- Assignments
ocw_type: CourseSection
title: Assignments
uid: b2fe6f42-3ae4-25b1-24ae-8a0145f03914
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---

{{< tableopen >}}
{{< theadopen >}}
{{< tropen >}}
{{< thopen >}}
SES #
{{< thclose >}}
{{< thopen >}}
ASSIGNMENTS
{{< thclose >}}
{{< thopen >}}
SUPPORTING FILES
{{< thclose >}}

{{< trclose >}}

{{< theadclose >}}
{{< tropen >}}
{{< tdopen >}}
1
{{< tdclose >}}
{{< tdopen >}}
Introduction to C
{{< tdclose >}}
{{< tdopen >}}
hello\_world.c ({{% resource_link e47750c4-b1d3-f389-40e8-abc7b816d0bc "C" %}})
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
2
{{< tdclose >}}
{{< tdopen >}}
Introduction to C memory management
{{< tdclose >}}
{{< tdopen >}}
({{% resource_link b3ddaddb-65a3-4b65-963d-bb9214af0fbf "ZIP" %}}) (This ZIP file contains: 2 .c files and 1 .h file.)
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
3
{{< tdclose >}}
{{< tdopen >}}
More C memory management
{{< tdclose >}}
{{< tdopen >}}
({{% resource_link b8d0170b-83b0-1a51-fe78-7d8e256e64c7 "ZIP" %}}) (This ZIP file contains: 1 .c files and 1 .h file.)
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
4
{{< tdclose >}}
{{< tdopen >}}
Introduction to C++
{{< tdclose >}}
{{< tdopen >}}
({{% resource_link 1d2ef4e0-aa9d-b3b9-89d6-c161c51ceadf "ZIP" %}}) (This ZIP file contains: 1 .cc files and 1 .h file.)
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
5
{{< tdclose >}}
{{< tdopen >}}
Inheritance and polymorphism
{{< tdclose >}}
{{< tdopen >}}
({{% resource_link 07327535-35b6-9d1f-227b-f8f9e72fbae2 "ZIP" %}}) (This ZIP file contains: 1 .cc files and 1 .h file.)
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

Assignment 1: Introduction to C
-------------------------------

1.  Obtain GCC, either from installing (gcc.gnu.org) or from running it on MIT servers.
    
2.  Figure out how to run GDB (gdb) and Valgrind (valgrind).
    
3.  Compile and run the "hello world" program.
    
4.  Extend the "hello world" program to print the current time. **Hint:** look at C's ctime (time.h) library.
    
5.  Submit your modified hello\_world.c program along with a README that describes 1) the command(s) you used to compile your program and 2) the command(s) you used to run your program. Please put the files into a single compressed .zip or .tar.gz file.
    

Assignment 2: Introduction to C Memory Management
-------------------------------------------------

2.  Write insert, find\_val, and delete\_bst in code we have included.
3.  Write tests and make sure your code works.
    
4.  Use valgrind to see if your code leaks memory.
    
5.  Submit all of your files in a compressed .zip or .tar.gz file along with a README describing 1) the command(s) you used to compile your program and 2) the command(s) you used to test your program. If you choose to include tests, you should also describe them. If you used a Makefile, please include that as well.
    

Assignment 3: More C Memory Management
--------------------------------------

1.  Re-implement the binary search tree code using an array instead of a node\_t struct, using the given .h file.
    
2.  Compare the two implementations. Which is faster? When would you prefer one implementation over the other, and why?
    
3.  Include a README that includes your files, how to run/compile them, and your response to the above question.
    

Assignment 4: Introduction to C++
---------------------------------

In this assignment, you will re-implement the binary search tree using C++ classes.

1.  Download and study the given header file "BST.h". This defines the interface to the binary search tree class, and includes the functionality that you need to provide to the client of the tree.
    
2.  Implement the methods "insert", "find", and "print\_inorder". You can define as many extra classes/fields/methods as you need, but DO NOT modify the declarations for the existing methods (i.e. these three methods, along with the constructor & destructor). You may also reuse code from the previous assignments. Think about access control issues — what should be exposed to or hidden from the client?
    
3.  Write test cases to show that your methods work correctly. You may extend the given test file, test\_BST.cc.
4.  Answer the following questions, and put your responses in a text file called "answers.txt":
    
    > 4.1. Compare the implementation of the BST in this assignment to those from the previous ones (i.e. struct & array-based implementations). What are some of the differences? How do they affect the client of the BST?
    > 
    > 4.2. What is the representation invariant for the BST? How would you modify your code to ensure that the invariant holds?
    > 
    > 4.3. There are an infinite number of BSTs in this universe (theoretically), so it is impossible to test that your code works for all BSTs. What approach did you take to make sure it's correct? Are your test cases sufficient, and how do you know?
    
5.  Submit all of your files (\*.h, \*.cc, answers.txt) in a compressed .zip or .tar.gz file, along with a README describing (1) the command(s) you used to compile your program and (2) the command(s) you used to test your program. If you choose to include tests, you should also describe them. If you used a Makefile, please include that as well.
    

Assignment 5: Inheritance and Polymorphism
------------------------------------------

In this assignment, you will use concepts of inheritance and polymorphism in C++ to implement simple arithmetic expression trees.

1.  Download and study the given header file "Expression.h". This defines an abstract base class that represents the interface to all expression trees. In this assignment, you will be defining subclasses that implement this interface. At minimum, these subclasses should provide definition for "eval" and "print" functions (unless they are abstract classes themselves).
    
2.  Design a type hierarchy, with "Expression" at the top, that represents a set of simple arithmetic expressions. The operations in this set include binary operations such as addition, subtraction, multiplication, and division over real numbers (which you may represent using floats in C++), as well as the negation operation. For example, you should be able to represent an expression such as "(3.0 + 4) \* -(5.0)".
    
    **Hints:** Think about the following: What are the common characteristics or behaviors among different expressions? What are the differences? Which functions/fields should be inherited, and which should be implemented separately?
    
3.  Implement the methods "eval" and "print". The "eval" method evaluates the expression and returns the resulting float. For example, the expression "(3.0 + 4) \* -(5.0)" should return -35.0. The "print" method should print the raw (i.e. unevaluated) expression in the infix notation.
    
4.  Write test cases to show that your methods work correctly. Include your test cases in "test\_expression.cc".
    
5.  Answer the following questions, and put your responses in a text file called "answers.txt":
    
    > 5.1. Let us suppose that we want to add an extra operation "exponentiation" that takes a base expression and an exponent. How would you modify/extend your type hierarchy to do this?
    > 
    > 5.2. This time, we want to add an operation "sum" that takes an arbitrary list of reals and add them together. How would modify/extend your type hierarchy? Why?
    > 
    > 5.3. Does your design allow invalid or undefined mathematical expressions? Why or why not?
    
6.  Submit all of your files (\*.h, \*.cc, answers.txt) in a compressed .zip or .tar.gz file, along with a README describing (1) the command(s) you used to compile your program and (2) the command(s) you used to test your program. If you choose to include tests, you should also describe them. If you used a Makefile, please include that as well.