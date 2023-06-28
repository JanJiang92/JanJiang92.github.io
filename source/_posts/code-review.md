---
title: code_review
date: 2021-01-31 21:39:48
tags:
---
words:
serious performance overhead
concatenation

https://codereview.stackexchange.com/questions/86341/first-oop-in-c-car-example?newreg=3a18e9bf56f844aeaa8ecab46d777333

1.single responsibility principle
2.PascalCase for types only and camelCase for variables and functions/methods


https://codereview.stackexchange.com/questions/165851/c-string-operators/165852#165852

1.Don't include unnecessary headers
2.we prefer <cstring> to <string.h> 
3.only need <ostream> rather than <iostream>
4.Avoid importing all of namespace std
5. static diagnostics with g++ -weffc++ to find out the warning
6.BUG - be careful using a null pointer as sentinel

7.Add a move constructor
8. size_t(unsigned_int) is more appropriate than int as the type of the index.



When you design object oriented programs you want to try to follow the SOLID design principles.

convention has emerged that public properties and methods should be at the top of the class declaration so that the programmers working with you can easily find them


---------------------------
1000 c++ MCQS
1.1.overloading is an example of static polymorphism, while overriding is an example of dynamic polymorphism.
1.2. Every static member function of a class must be initialized explicitly before use and a data member
1.3. all the constant variables must be initialized while declaration
     pointer with const 
     https://www.geeksforgeeks.org/difference-between-const-int-const-int-const-and-int-const/#:~:text=This%20means%20that%20the%20variable,that%20shouldn't%20be%20changed.&text=The%20first%20const%20keyword%20can,is%20equivalent%20to%20const%20int*.