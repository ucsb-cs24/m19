---
num: "lect04"
desc: "Linked Lists, Operator overloading, Unit tests"
ready: true
pdfurl: /lectures/CS24_Lecture4.pdf
annotatedpdfurl: /lectures/CS24_Lecture4_ann.pdf
annotatedready: true
lecture_date: 2019-04-10
---

# Code from lecture

[{{site.lect_repo}}/tree/master/lec-04]({{site.lect_repo}}/tree/master/lec-04)

# Topics

## Linked Lists

* Linked lists as an ADT (implementation using classes)


## Unit testing

* We'll go over some important [guidelines related to unit testing](https://petroware.no/unittesting.html)

* I suggest also reading [this blog post](http://blog.stevensanderson.com/2009/08/24/writing-great-unit-tests-best-and-worst-practises/) about the best (and worst) practices for unittesting your code

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










