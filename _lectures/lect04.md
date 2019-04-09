---
num: "lect04"
desc: "Linked Lists, Operator overloading, Unit tests"
ready: true
pdfurl: /lectures/CS24_Lecture4.pdf
annotatedpdfurl: /lectures/CS24_Lecture4_ann.pdf
annotatedready: true
lecture_date: 2019-01-16
---

# Code from lecture

[https://github.com/ucsb-cs24-w19-mirza/cs24-w19-lectures/tree/master/lec-04](https://github.com/ucsb-cs24-w19-mirza/cs24-w19-lectures/tree/master/lec-04)

# Topics

## Linked Lists

* Linked lists as an ADT (implementation using classes)

* Revisit the big four for linked list

C++ provides a default constructor, destructor, copy constructor, copy assignment operator for any class that doesn't have one explicitly defined.


## Makefiles and unit testing
* We will split our implementation of linked list into three files  - header file (contains only the class definition), source file (contains the implementation of the class methods - no main), test file - uses the ADT. (More practice on this in lab02)
* Write a simple Makefile to compile all the different programs written in class

## Non member functions and friend functions
* If a non-member function is declared to be a friend of a class, it can access the private members of the class.
* Discuss when/why you might use friend functions

## Operator overloading - Pages 63 - 80 in the book

We will overload some of the operators for the Quadratic and Linked List classes.

Example from reading:

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










