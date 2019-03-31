---
num: pa02-checkpoint
ready: true
desc: "Linked-list implementation of a card game"
assigned: 2019-01-28 09:00:00.00-8
due: 2019-02-06 23:59:00.00-8
---

<div markdown="1">

## This assignment may be done solo or in pairs.

# Introduction

* The first thing you need to do for the checkpoint is read the description for the project here: [https://ucsb-cs24.github.io/w19/pa/pa02/](https://ucsb-cs24.github.io/w19/pa/pa02). Though you don't need to have all of this implemented by the checkpoint, it is essential that you have a good idea where this project is going so that you are able to make good design decisions. 

# Instructions

The goal of the checkpoint is to get you thinking about how you plan on completing the rest of the assignment before jumping into coding it as well as to allow us to give you some initial feedback on your approach. Make sure you've read the entire project description carefully and spend some time thinking about what functionality your card list needs to have as well as how you will leverage this to code the game. 

## Design approach

For the checkpoint, you submit exactly six files with the names: Makefile, main.cpp, cards.cpp, cards.h, gameplan.cpp, testcards.cpp


* In cards.h, provide the definition of all the classes that you will use for this PA. You may define multiple classes in the same file. Prior to the definition of each class, write the pre-and post conditions for all the public member functions and non-member functions as a commented header (follow the style of stats.h from pa01). One of your classes must define a linked list to store cards.
 
* Create stubs for class functions you will need (you must ensure that your `cards.h` and `cards.cpp` files still compile so that you can compile and run the test code. Don't implement any of the public functions yet.

* In testcards.cpp, write code to unit test your class implementation.
Organize your test code, so that there is one test function corresponding to each class, called test_<className>(). This function should in turn call other functions to unittest each of the memmber functions of that class. Write one test function to unit test each member function of each class, follow the naming convention: test_<className>_<memberFunction>(). Each of these functions should contain multiple test cases, paying special attention to edge cases. You may use other helper functions to organize your test code. You must test all the methods of your linked list, even if you plan to reuse your implementation from lab02.

* Write a Makefile that produces two executables- game and unittest. The game executable should be compiled from cards.cpp and main.cpp and corresponds to your implementation of the game. The unittest executable should be compiled from cards.cpp and testcards.cpp and should run all of the unittests.

* In cards.cpp, implement the method(s) to store card hands in a linked list (though it does not need to have the full game functionality yet) and to print the entire card hand for a player. 

* In main.cpp, implement the portion of your code required to read each player's cards from a file, store them in linked lists, and print each players hand. This portion will be autograded on gradescope. See an example of the expected behavior below:

## Example for checkpoint:

Contents of `alice_cards.txt`:

```
h 3
s 2
c a
c 3
h 9
s a
```

Contents of `bob_cards.txt`:

```
c 2
s a
d j
h 9
c 3
```

Correct output after running `make && ./game alice_cards.txt bob_cards.txt`:

```
Alice's cards:
h 3
s 2
c a
c 3
h 9
s a

Bob's cards:
c 2
s a
d j
h 9
c 3
```

* Create a gameplan.cpp,  which details how you will use your classes  to run the game. This can either be in code which makes calls to the stubs you've defined or psuedo-code which details how you will use these functions once they are fully defined. This `gameplan.cpp` is the start of your main for the final turn in for this project. 

* Your main focus when completing this section should be to clarify your thoughts on your code structure for this project and communicate that with your mentor.

# Submission instructions 

You must submit exactly six files with the names: Makefile, main.cpp, cards.cpp, cards.h, gameplan.cpp, testcards.cpp

Submit these files to PA02-Checkpoint on gradescope. You should score 100% if you have completed the linked list implementation portion of this project. The rest of the points for this checkpoint will be given by your mentor who will check that you have completed the design approach portion of this project and your code style. 

Also push your code on github. Include the commit message "CHECKPOINT SUBMISSION" when pushing your code to github. 

Created by Jack Alexander, Jinjin Shao, Sierra Schwellenbach, and Diba Mirza
