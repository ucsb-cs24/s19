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

* movies.cpp, movies.h    // These files should contain your implementation of the binary search tree to store movies information
* utility.cpp, utility.h // These files should contain any other classes that you need to implement your game,
* tests.cpp, tests.h // These files should contain test code for all the classes and methods you used in your game
* main.cpp // This file should read in the movies from input files and create BST along with functionality to time the searches / other functions.
* Makefile // generate two executables- the first should be called ```movies``` and the second should be called ```tests```. The command ```make tests``` should RUN (not just compile) all the test code to unit test your classes and methods 

## Approach
You are given 3 pairs of input files, each pair contains 20,100 and 1000 movies respectively. The only difference between files in a pair is the way movies are ordered. In one case movies appear alphabetically in the file while in the other case they appear in random order.  As discussed in the lecture, the order of inserting values into a BST affects its structure and hence the running time. Your goal is to investigate how the running time of search relates to the depth of a movie in the BST. The depth of a movie in the BST is the number of nodes on the path from the root to the node containing the movie. For example, the root will be at depth 0.



The file will be of this format [File1](input_20_ordered.csv) and [File2](input_20_random.csv).
You will then create your BST and insert the movies in the same order as that of the files. The node in BST will store information such as movie_name, rating, level. Sample execution of the program will be as follows:
`./movies arg1 arg2 arg3`. `arg1`  represents the flag which is a boolean variable i.e. can be `true` or `false`. `arg2` represents the input file which is to be inserted into the BST. `arg3` will either be a movie prefix if the flag is true or the name of the output file if the flag is false. 
Once inserted, there are again two modes of operation. If true, you need to print the pre-order traversal of your tree which consists of node data i.e. movie name and level. Then you need to search for the movie with the highest rating beginning with the prefix that is passed as the 3rd argument. If the flag is false, you need to search for all the movies in the BST i.e. perform search on each movie present in the input file/BST. You also need to time your searches and store statistics such as minimum, maximum and median time taken to perform search across all movies. You also need to track the number of steps that occurred during the search. You can use the output file to store all the timing and steps taken for search operations.
Here is an exmaple of execution:
`./movies true input_20_ordered.csv harry`
Here, the  flag is `true`, input file is `input_20_ordered.csv` and `harry` is the prefix. Now, the program should insert all the movies in input_20_ordered.csv, then print the pre ordered traversal and also the movie name with highest rating which has harry as its prefix. And
`./movies false input_20_ordered.csv output.txt`
Here, the flag is `false`, input file is `input_20_ordered.csv` and ouptut file is `output.txt`. Now, the program should insert all the movies in input_20_ordered.csv, then calcualte the time and steps done for the search for each movie. You can store the information in the output file in the format you desire. You will be using this for your report.


## Requirements
For this programming assignment, you will have a lot of flexibility on your implementation (which just means we won't be providing a code framework for you to fill in). However, there are a few requirements that you need to keep in mind as you think about your solution:

* You must use a binary search tree you implemented yourself to solve the problem, not another data structure or a class in the standard library.
* Your binary search tree must implement a constructor, a destructor and other methods as needed
* You must time and report your search/lookup function calls
* Your code should be readable
* Your classes should define clear interfaces and hide implementation details as much as possible. 
* Your program must properly free all memory it allocates, including your binary tree nodes and any dynamically allocated data stored inside them. We will also check this with valgrind when you turn in your code to Gradescope.

## Report
Here is the sample [sheet](https://docs.google.com/spreadsheets/d/1E85wYZuRcF60yQlmdd72TdSxLqhi7c6WJYAO1tt-qTM/edit?usp=sharing) to create graphs and [document](https://docs.google.com/document/d/1XHuhM1U0ItWX1GRv--A1Th-qtrjfEoGjqdfXjXkJAAw/edit?usp=sharing) format expected for the report.
First, you need to collect the minimum, maximum and median time taken for search for each input file. You need to run your executable for each input file for 10 times and then calculate the average time taken for each input file. Meaning, you need to call `./movies false input_1.csv output_1.txt` 10 times and then find average timings for input_1.csv. Then you need to do the same for the rest of the 5 input files.
You also need to calculate the total number of steps taken for each search for 1000_ordered and 1000_random files and plot them in the graph as shown in the link above.

# Submission instructions 

Submit your code on Gradescope. You must organize your program in the files: `main.cpp`, `movies.cpp`, `tests.cpp`, `movies.h`,`tests.h`, `utility.cpp` and `utility.h` Also, you must create a `Makefile` that compiles your program to an executable called `movies` and `tests`.
In addition, you have to submit a report on Gradescope containing your time values searches. 
