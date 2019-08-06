---
num: "lect06"
desc: "Rule of Three, GDB, intro to pa01"
ready: true
pdfurl: /lectures/CS24_Lecture6.pdf
annotatedpdfurl: /lectures/CS24_Lecture6_ann.pdf
annotatedready: true
lecture_date: 2019-04-16
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


## Rule of three
* In C++ there is a rule of thumb that states if any of the copy-constructor, copy assignment or destructor are overloaded, the others must be overloaded as well. We's like to understand the reasoning behind this rule of thumb. We looked at why and how we need to overload the destructor and the copy-constructor in the last class. We'll focus on the copy assignment operator in this class.

The questions we ask are:
1. What is the behavior of these defaults (taking linked lists as our running example)?
2. When and why do we need to overload these? 
3. What is the outcome we desire to have with the overloaded de'tor, copy con'tor and copy assignment operator for the linked list class?

## Destructor

In general the destructor is called when 
a) a stack object goes out of local scope and has to be removed from memory
b) delete is called on a pointer that is pointing to an object of the class on the heap

Here are two scenarios where the destructor is called

Case 1:
```
void foo(){
   LinkedList l1; 
   ....
   ....
   //l1's destructor is called  right after the function returns
}

```
Case 2:

```
  LinkedList* p = new LinkedList; // This line may be in any function
  .....
  delete p; // This line may be in a function different from where the object was created with new
```

Now suppose we had a linked list object (either on the stack or the heap) that has the following elements

```
l1:1->2->5->null
```  
* What is the state of memory after l1's default destructor is called?
* Do you see a problem with the default behavior?
* How would you fix this problem?


## Copy constructor

The default copy constructor copies the values of the member variables of a source object to the objects that is being created.

For we created the following linked list in memory:
```
l1:1->2->5->null
```
As far as the compiler is concerened its perfectly valid to create a new object l2 that is the copy of l1 as follows:

```
LinkedList l2(l1); // l2's copy constructor is called and l1 is passed as a parameter
```
OR 

```
LinkedList l2 = l1; // l2's copy constructor is called and l1 is passed as a parameter
```

OR we could create the new object on the heap as follows

```
LinkedList* p = new LinkedList(l1); 
```

In all the above cases the default copy constructor of the new object is called. 

* What is the state of memory in each case?
* Do you see a problem with the default behavior? (Talk about shallow vs deep copy)
* How can we fix this problem?


## Copy assignment operator

The default assignment operator works like the copy constructor except it copies values from one existing object to another object that already exists

For we had two linked lists in memory:
```
l1:1->2->5->null
```
```
l2:10->20->50->60->null
```

The copy assignment operator will be called in all of the following cases: 

```
l2 = l1; // l2's copy assignment is called and l1 is passed as a parameter
```
OR 

```
l2 = l2; //l2's copy assignment is called and l2 is passed as a parameter!
``` 

* What is the state of memory in each case?
* Do you see a problem with the default behavior? 
* How can we fix this problem? Describe the desired behavior





