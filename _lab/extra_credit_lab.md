---
num: extra_credit_lab
ready: true
desc: "Statistician as a C++ Abstract Data Type (ADT)"
assigned: 2019-05-09 09:00:00.00-8
due: 2019-06-07 23:59:00.00-8
---

<div markdown="1">

## {{page.num}} must be done individually&mdash;each student must accomplish it
alone and submit it. 


## Create a git repo and obtain the starter code

* Create a git repo named <tt>{{page.num}}_your_github_username<tt> in our class organization, [{{site.class_org.name}}]({{site.class_org.url}}).

* Clone your repo on CSIL in your home directory.

* Get the starter code : If you have already cloned the `cs24-s19-starter-code`
change into it and type `git pull` to get the latest starter code.

* Change into your repo directory and obtain copy the starter code by
   typing the following command
   ```
   cp ~/cs24/cs24-s19-starter-code/extra_credit_lab/* ./

   ```

## Assignment instructions

Files to submit: `stats.h`, `stats.cpp` `stattest.cpp` and a `Makefile`

This assignment is based on Chapter 2, Programming Project 2 and 3
(here is a local copy of [page 90](Page-90.pdf). Follow the instructions on this web page, not the
ones on page 90 - but do see the hints provided by the textbook
author.

1. Type your name and the date in a comment at the top.(Like always, whether or not we remind you!)

2. Write unit tests in the file: `unittests.cpp`
   This code should test each of the public interfaces and non member functions of your class and follow the structure described in lecture 4. 

3. Complete the incomplete definition of class statistician as
   provided in `stats.h` header file. In particular you must reason
   about the attributes of the statistician. Define the private member
   variables.

4. Write a `Makefile` to compile your code with both the test files. 

5. Implement the constructor, all the member functions, and all three
   non-member functions. Note that a subset of the non-member functions should be
   declared as friend functions (friend function grant you access to statisticians' private fields, 
   and you won't have to define additional getters and setters). Read the documentation for each of these
   functions at the top of `stats.h`, and make sure your implementations
   work as advertised in those comments - i.e., satisfy all of the
   postconditions.

6. Submit the files for {{page.num}} on gradescope: `stats.h`, `stats.cpp`, `stattest.cpp`, `unittests.cpp`, 
   `Makefile`. Be sure to wait for the results of all tests. If you
   score 80/80, and you've followed all of the other rules, then
   you'll earn 80/80. The additional 20 points will be manually graded for writing appropriate test code, and Makefile, and good coding style.


## Some hints:

* Use assert to verify the pre-conditions of functions mean, minimum and maximum.

* Compile and test your program at CSIL (connecting remotely is okay).




