# Introduction

* Create a GitHub repo following the correct naming convention.
* If you have a partner, add your partner as a collaborator to the repo. The partner should accept the invitations to complete this process
* You and your partner should agree to use pair programming to complete the pa instead of dividing the work and coding separate parts of the pa individually
* Minimal starter code is provided for this lab, but be sure to grab it from GitHub


# Goal of this assignment

* Practice implementing and using Binary Search Trees
* Learn to perform runtime complexity analysis and express your analysis using Big-O notation
* Learn to organize a project's code structure on your own (not just filling in a template)
* Learn to design classes using good OOP design principles discussed in class
* Learn to test your code using unit test cases


# Instructions

In this assignment we have given you datasets containing movie names and their rating. Your goal is to implement a Binary Search Tree to store this information, measure and analyze the running time of searching for movies.

An overview of your goals are provided below:
* Implement a Binary Search Tree to store movie names and ratings.
* Your BST should provide public function to search for a "particular" movie, search for movies that start with a specific prefix, and calculate the average rating of movies that start with a prefix.
* Measure the absolute running time of your search functions and how it scales with input size.
* Analyze the Big-O running time for different types of search.
* Write a report to discuss the trends in running times using your mathematical analysis to explain the performance data that you collected.
 
## Required Files

* movies.cpp, movies.h    // These files should contain your implementation of the binary search tree to store movies information
* utility.cpp, utility.h // These files should contain any other classes that you need to implement your game,
* tests.cpp, tests.h // These files should contain test code for all the classes and methods you used in your game
* main.cpp // This file should read in the movies from input files and create BST along with functionality to time the searches / other functions.
* Makefile // generate two executables- the first should be called ```movies``` and the second should be called ```tests```. The command ```make tests``` should RUN (not just compile) all the test code to unit test your classes and methods 

## Approach
You are given 3 pairs of input files, each pair contains 20,100 and 1000 movies respectively. The only difference between files in a pair is the way movies are ordered. In one case movies appear alphabetically in the file while in the other case they appear in random order.  As discussed in lecture, the order of inserting values into a BST affect its structure and hence the running time. Your goal is to investigate how the running time of search relates to the "depth" of a movie in the BST. The depth of a movie in the BST is the number of edges on the path from the root to the node containing the movie. For example, the root is at depth 0.



The file will be of this format File1(input_1.csv) and File2(input_2.csv).
You will then create your BST and insert the movies in the same order as that of the files. The node in BST will store information such as movie_name, rating, level. You will also be given two movie names for each pair that needs to be searched. You need to search for these two movies along with your "favorite" movie among the movies given in the input file but different from those provided by us. You also have to time your search (using time.h or other libraries) and then report them in a seperate file. So for each input file, you will record 3 searches and in total, you should have 18 records.  You will also implement an extra function that will compute the average of all movies that begin with a particular letter (passed as input). An example of execution is 
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
