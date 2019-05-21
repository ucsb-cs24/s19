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

In this assignment, we have given you datasets containing movie names and their ratings. Your goal is to implement a Binary Search Tree to store this information, measure and analyze the running time of searching for movies.

An overview of your goals are provided below:
* Implement a Binary Search Tree to store movie names and ratings.
* Your BST should provide a public function to search for a particular movie, search for movies that start with a specific prefix, and find the movie with the highest rating starting with a particular prefix.
* Measure the absolute running time of your search functions and how it scales with input size.
* Analyze the Big-O running time for different types of search.
* Write a report to discuss the trends in running times using your mathematical analysis to explain the performance data that you collected.
 
## Required Files

* ```movies.cpp, movies.h```    // These files should contain your implementation of the binary search tree to store movies information
* ```utility.cpp, utility.h``` // These files should contain any other classes that you need to implement your game,
* ```tests.cpp, tests.h``` // These files should contain test code for all the classes and methods you used in your game
* ```main.cpp``` // This file should read in the movies from input files and create BST along with functionality to time the searches / other functions.
* ```Makefile``` // generate two executables- the first should be called ```movies``` and the second should be called ```tests```. The command ```make tests``` should RUN (not just compile) all the test code to unit test your classes and methods 

## Starter Code
As in previous assignments the starter code is available in the repo: [https://github.com/ucsb-cs24-s19-mirza/cs24-s19-starter-code](https://github.com/ucsb-cs24-s19-mirza/cs24-s19-starter-code)
The starter code has the following files
* ```main.cpp``` // Skeleton code to read in movies from input files
* ```input_20_ordered.csv```
* ```input_20_random.csv```
* ```input_100_ordered.csv```
* ```input_100_random.csv```
* ```input_1000_ordered.csv```
* ```input_1000_random.csv``` 

You are given 3 pairs of input files, each pair contains 20,100 and 1000 movies respectively. The only difference between files in a pair is the way movies are ordered. In one case movies appear alphabetically in the file while in the other case they appear in random order. The files are of format [File1](input_20_ordered.csv) and [File2](input_20_random.csv).

## Approach
As discussed in the lecture, the order of inserting values into a BST affects its structure and hence the running time. Your goal is to investigate how the running time of search relates to the depth of a movie in the BST. The depth of a movie in the BST is the number of nodes on the path from the root to the node containing the movie. For example, the root will be at depth 0.

In this assignment, we ask that you implement your own BST class. One of the variations to your BST compared to an earlier lab is that each node in your BST should store information such as movie_name, rating, depth. Your main program should expect three arguments from the user. A sample execution of the program will be as follows:

`./movies arg1 arg2 arg3`

`arg1`  is a boolean flag, which can be `true` or `false`
`arg2` represents the input file containing movies and ratings (as described before)
`arg3` is either the starting letters of a movie name (movie prefix) or a number

You should use the value of the flag(`arg1`) to interpret the third argument and accordingly do one of two things:

## Case 1: Find the highest rated movie that starts with a given prefix
If `arg1` is `true`, you should expect the third argument to be a movie prefix. In this case, 
* In your main program insert the movies in the same order as they appear in the input file into a BST, using the public functions of your class. 
* Print the pre-order traversal of your tree to stdout, for each node visited, output the movie name, rating, and depth. 
* Find the movie with the highest rating beginning with the prefix was passed in as the third argument, using the public functions of your BST.

Below is a sample run of the program with `arg1` as `true`
```
./movies true input_20_random.csv the
```
This should produce the following output:
```
toy story, 7.7, 0
jumanji, 6.9, 1
grumpier old men, 6.5, 2
father of the bride part ii, 5.7, 3
dracula: dead and loving it, 5.7, 4
balto, 7.1, 5
ace ventura: when nature calls, 6.1, 6
cutthroat island, 5.7, 6
casino, 7.8, 7
goldeneye, 6.6, 4
four rooms, 6.5, 5
heat, 7.7, 3
sabrina, 6.2, 2
nixon, 7.1, 3
money train, 5.4, 4
tom and huck, 5.4, 3
sudden death, 5.5, 4
sense and sensibility, 7.2, 5
the american president, 6.5, 5
waiting to exhale, 6.1, 1

Best movie is the american president with rating 6.5
```

## Case 2: Analyze the time to search for keys in a BST and write a report
If `arg1` is `false`, your goal is to collect two types of timing data to answer the following questions: 
(1) What are the statistics of the **average time to search in a BST**?  
(2) How does **the number of primitive operations to search in a BST** vary with the depth of a node? 

Note that you need to collect two different types of data to answer these questions. The first is an absolute time, while the second is a count. 

To answer (1), calculate the average time to search for any key. You can calculate this as the total time it takes to search for all the keys in your BST divided by the number of nodes in the BST. To get a more reliable value, don’t time each search. If your BST has N keys, record the time it takes to perform all N searches and then divide that value by N. You should expect this average time to have some random variation, which is why we ask that you compute it over multiple (W) runs and report the min, max and median statistics. The value of W is the third argument to your program. We recommend that you use a W value of 10 in all cases, but your program should work for any W.

To answer (2), write code in your BST implementation that tracks the number of steps that occurred during the search operation. Search for all the keys in your BST, and record how the number of primitive steps varies with the depth of the node that stores that key.  You can choose to store the data in an output file in two columns: **depth** and **number of steps to search**. Note that in this case, there is no randomness and you don't need to calculate averages. Collect this data for input files: ```input_1000_ordered``` and ```input_1000_random```. Plot your data for both cases showing a scatter plot of the number of operations vs. depth. 
Here is a [sample sheet](https://docs.google.com/spreadsheets/d/1E85wYZuRcF60yQlmdd72TdSxLqhi7c6WJYAO1tt-qTM/edit?usp=sharing) to create the graph.

Write a **report** to present the data and explain the trends for the data collected for (1) and (2).
Here is a [sample report](https://docs.google.com/document/d/1XHuhM1U0ItWX1GRv--A1Th-qtrjfEoGjqdfXjXkJAAw/edit?usp=sharing) format expected for the report.

Case 2 will be manually graded. The autograder will just check that your program compiles and runs without crashing for this case.

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
In addition, you have to submit a report as a pdf file on Gradescope, the assignment is called pa02-report.
