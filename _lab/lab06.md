---
layout: lab
num: lab06
ready: true
desc: "Implementing a heap"
assigned: 2019-05-28 13:00:00.00-8
due: 2019-06-03 23:59:00.00-7
---

# Goals for this lab

By the time you have completed this lab, you should be able to

* Understand the purpose and behavior of a priority queue
* Understand how to implement an array-based heap

This lab may be done with a partner

## Step by Step Instructions

# Step 0: Complete the TA/Mentor evaluations
As you may know, we ran a pilot mentor program this quarter.
We would like to get your feedback about the program to help us keep the aspects that worked well and identify areas for improvement.

Completing the survey carries course credit (1% of your overall grade), so please be sure to complete it. This is an anonymous survey. To get credit please show the final screen  to the instructor TA/tutor

Here is the link to the survey:
[Please click on this link to complete](http://bit.ly/2018-Anonymous-Mentor-Evals)


To get credit show a screenshot of the final page of the completed survey on gradescope (lab06) to your TA. They will record your grade manually.

For more imformation, you can look at the lecture slides for heap and its implementation - [heap](https://ucsb-cs24.github.io/w19/lectures/CS24_Lecture13.pdf) and [heap implementation](https://ucsb-cs24.github.io/w19/lectures/CS24_Lecture14.pdf)

## Step 1: Create a lab06 git repo and get the starter code

First get together with your lab partner. If your regular partner is more than 5 minutes late, let your mentor know.

Select a pilot, log into the CSIL machines.

## Step 1a: Create a git repo, add your partner as collaborator

* Create a repo for this lab on the pilot's github account (just like you did in lab00): To do this, open a browser and navigate to [www.github.com](www.github.com). Log into the pilot's github account. From the drop down menu on the left, select our class organization: ucsb-cs24-s19-mirza and proceed to create a new repo. You may refer to the instructions in lab00. Follow this naming convention: If your github username is jgaucho and your partner's is alily, your should name your repo lab06_agaucho_alily (usernames appear in alphabetical order). Also you must set the visibity of your repo to be 'PRIVATE' when creating it. We will not repeat these instructions in subsequent labs.

* The pilot should add the navigator as a collaborator on github, and the navigator should accept the request to join the repo. See instructions in previous labs

## Step 1b: Clone your git repo and get the starter code

* Create a git repo and get the starter code.

You should have the following files:

```
-bash-4.3$ ls
examheap.cpp heap.cpp heap.h
```

First look at heap.h to see the basic operations for a heap. You will implement all of these operations for these lab. Also notice the storage mechanism we will be using for the heap: a [http://www.cplusplus.com/reference/vector/](vector). It will probably be a good idea to read through the documentation for this standard library class (linked above) if you are not familiar with it.

Now look at examheap.cpp. This file will test your heap's behavior. The first test is quite simple and just adds a couple elements to your heap. For larger numbers of inputs, it uses the `std::priority_queue` class from the standard library as ground truth to test your code against. The first thing you need to do is compose your Makefile to compile `examheap.cpp` with `heap.cpp` to executable `examheap`. Then, feel free to compile and run `examheap` before starting on your code. However, note that all the tests will fail and say "Aborted (core dumped)".

## Step 2: Implement the functions of heap.cpp

There are four functions you need to implement in heap.cpp: `push`, `pop`, `top`, and `empty`. Note that only `push` and `pop` modify the heap, while `empty` and `top` only return values. When testing your code, be sure to run the large tests (4 and 5) to find any minor bugs in your code that may not show up on the smaller tests.

You are allowed to add helper functions in heap.h and heap.cpp if you need them. However, you should use the vector in heap.h as the underlying storage for your heap.

## Step 3: Submit heap.cpp and heap.h

Submit the files heap.cpp, heap.h, and Makefile to the lab06 assignment on Gradescope.

## Evaluation and Grading

Each student must accomplish the following to earn full credit for this lab:
[70 points] heap.cpp and heap.h are saved, with your name(s) in a comment at the top and other evidence of your work. Both of these files should compile and execute properly too.


