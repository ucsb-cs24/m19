---
num: "lect07"
desc: "Recursion (contd), GDB, Binary Search Trees"
ready: true
pdfurl: /lectures/CS24_Lecture7.pdf
annotatedpdfurl: /lectures/CS24_Lecture7_ann.pdf
annotatedready: false
lecture_date: 2019-08-21
---

# Code from lecture
[{{site.lect_repo}}/tree/master/lec-07]({{site.lect_repo}}/tree/master/lec-07)


# Recursion
* Practice recursion on linked-lists
* Recursive implementation of binary search
* Intro to Binary Search Trees

## gdb

* Demo of gdb commands 
 - To use gdb, compile with the -g flag
 - Setting breakpoints (b)
 - Running programs that take arguments within gdb (r arguments)
 - Continue execution until breakpoint is reached (c)
 - Stepping into functions with step (s)
 - Stepping over functions with next (n)
 - Re-running a program (r)
 - Examining local variables  (info locals)
 - Printing the value of variables with print (p)
 - Quitting gdb (q)
 - Debugging segfaults with backtrace (bt)
* Refer to the [gdb cheat sheet]({{site.lect_notes}}/GDB-cheatsheet.pdf) (handout given in class). More practice in lab 03.
