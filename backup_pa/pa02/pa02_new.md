# Introduction

* Create a GitHub repo following the correct naming convention.
* If you have a partner, add your partner as a collaborator to the repo. The partner should accept the invitations to complete this process
* Minimal starter code is provided for this lab, but be sure to grab it from GitHub


# Goal of this assignment

* Practice using Binary Search Trees
* Learn to perform runtime analysis/time complexity and denote in O() notations
* Learn to organize a project's code structure on your own (not just filling in a template)
* Learn to design classes using good OOP design principles discussed in class
* Learn to test your code using unit test cases


# Instructions

In this assignment:

* You will be given files containing movie names along with ratings.
* You will implement and use Binary Search Tree to store the above information.
* You will then perform searches for "particular" movie names and time then.
* You will do run time analysis on time taken for searches and write a report on it.
* You will also implement a function to compute average ratings of all movies beginning with a particular character. 

## Required Files

* movies.cpp, movies.h    // These files should contain your implementation of the binary search tree to store movies information
* utility.cpp, utility.h // These files should contain any other classes that you need to implement your game,
* tests.cpp, tests.h // These files should contain test code for all the classes and methods you used in your game
* main.cpp // This file should read in the movies from input files and create BST along with functionality to time the searches / other functions.
* Makefile // generate two executables- the first should be called movies and the second should be called tests and must RUN (not just compile) all the test code to unit test your classes and methods 

## Approach
You will be given 3 pair of input files, each pair containing 20,100 and 1000 movies respectively. The only difference between files in a pair is the way they are ordered. One of them in alphabetically ordered and the other is not.  The file will be of this format File1(input_1.csv) and File2(input_2.csv). You will then create your BST and insert the movies in the same order as that of the files. The node in BST will store information such as movie_name, rating, level. The level is the number of edges from the root i.e. height. For example, the root will at level 0. You will also be given two movie names for each pair that needs to be searched. You need to search for these two movies along with your "favorite" movie ( which is present in the file but is not the same as the movies given by us). You also have to time your search (using time.h or other libraries) and then report them in a seperate file. So for each input file, you will record 3 searches and in total, you should have 18 records.  You will also implement an extra function that will compute the average of all movies that begin with a particular letter (passed as input). An example of execution is 
`make && ./movies input_1.txt movie_a movie_b movie_c some_letter`

## Requirements
For this programming assignment, you will have a lot of flexibility on your implementation (which just means we won't be providing a code framework for you to fill in). However, there are a few requirements that you need to keep in mind as you think about your solution:

* You must use a binary search tree you implemented yourself to solve the problem, not another data structure or a class in the standard library.
* Your binary search tree must implement a constructor, a destructor and other methods as needed
* You must time and report your search/lookup function calls
* Your code should be readable
* Your classes should define clear interfaces and hide implementation details as much as possible. 
* Your program must properly free all memory it allocates, including your binary tree nodes and any dynamically allocated data stored inside them. We will also check this with valgrind when you turn in your code to Gradescope.

# Submission instructions 

Submit your code on Gradescope. You must organize your program in the files: `main.cpp`, `movies.cpp`, `tests.cpp`, `movies.h`,`tests.h`, `utility.cpp` and `utility.h` Also, you must create a `Makefile` that compiles your program to an executable called `movies` and `tests`.
In addition, you have to submit a report on Gradescope containing your time values searches. 
