---
num: "lect06"
desc: "Intro to pa01, operator overloading, GDB"
ready: true
pdfurl: /lectures/CS24_Lecture6.pdf
annotatedpdfurl: /lectures/CS24_Lecture6_ann.pdf
annotatedready: false
lecture_date: 2019-08-20
---

# Code from lecture
[{{site.lect_repo}}/tree/master/lec-05]({{site.lect_repo}}/tree/master/lec-06)

# Topics

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
* Refer to the [gdb cheat sheet](http://darkdust.net/files/GDB%20Cheat%20Sheet.pdf) (handout given in class). More practice in lab 03.

