---
num: "lect03"
desc:  "The Big Four, Operator Overloading "
ready: true
pdfurl: /lectures/CS24_Lecture3.pdf
annotatedpdfurl: /lectures/CS24_Lecture3_ann.pdf
annotatedready: false
lecture_date: 2019-04-08
---

# Code from lecture:

[https://github.com/ucsb-cs24-s19-mirza/cs24-s19-lectures/tree/master/lec-03](https://github.com/ucsb-cs24-w19-mirza/cs24-s19-lectures/tree/master/lec-03)

# Topics

## The big four
* Constructor 
 	- Default and parameterized constructors (Review)
	- Initializing const member variables using initialization lists
* Destructor
* Copy-constructor
* Copy-assignment

## Non member functions and friend functions
* If a non-member function is declared to be a friend of a class, it can access the private members of the class.
* Discuss when/why you might use friend functions


## Makefiles
* We will split our implementation of the die Game from the previous class into three files  - header file (contains only the class definition), source file (contains the implementation of the class methods - no main), test file - uses the ADT. (More practice on this in lab02)
* Write a simple Makefile to compile all the different programs written in class



## Operator overloading - Pages 63 - 80 in the book

We will start with a basic implementation of the point class from Chapter 2. We will then augment the class with binary operator functions. By **overloading** certain operators like ==, we can now write code as shown below:

```
point p1, p2;
if (p1 == p2){
  cout<<"Points are equal\n";
}
```
We will specifically discuss:

1. Overloading binary comparison operators e.g. ==
2. Overloading binary arithmetic operators e.g. +
3. Overloading output and input operators e.g. >> and <<






