---
title: new_c++
date: 2020-12-02 21:28:34
tags:
---

C++ Interview questions:
1.each level of function has its own stack frame
2.delete keyword
3.the size of a struct equal to the sum of the sizes of the variables that are stored within it: much more efficient for the compiler to store things within blocks of four bytes based on the way that memory addresses work
4. purpose of using #ifdef and #if: 
   4.1.control the flow of code from make-file, cross-platform programming, easy switch between debug and release mode, making include guards
   4.2.include guards - avoiding #include the same file twice[#ifdef](https://stackoverflow.com/questions/33117233/what-does-purpose-use-ifdef-and-if-in-c)
5. null(with that compiler would be confused and treat it either as pointer or number 0) and nullptr-a null of pointer with the value of null
6. just in your scope using namespace std rather than declare it in hte head file
 keyword: 
 0. dot(.) and arrow operator(->) [difference](https://stackoverflow.com/questions/1238613/what-is-the-difference-between-the-dot-operator-and-in-c):-> can be overloaded
 1.[explicit used in front of constructor](https://www.geeksforgeeks.org/g-fact-93/)
          useage: avoiding such implicit conversation, where the constructor with a single argument be implicitly handled.

 2.[ initializer_list<T>]   initialise the specific variables

 3. auto and decltype - uitilitzd to build up the Template:
    auto used to specify the variable with the particular type
    decltype: extract its type from variable
    eg. typedef declttype(vari_name) my_self_defined_type;     

 4.  Override & final
     with Override explicitly shown the function that is overrided to compiler to get ride of no detection by compiler when problem exists(e.g. refined the fct with different sigature)  (override)[https://stackoverflow.com/questions/18198314/what-is-the-override-keyword-in-c-used-for] final: protect the function of base class froming be overriding by the derived class.
            in a nutshell: avoiding itself overridded and derived 
 5. Lambda expression [capture clause](parameters)->return-type{ definition of method}

 6. mutable normally used in lamda and const subfunction 

 7.  overload << friend ostream& operator<<(ostream& output, const Box& B){
        output<<B.l<<' '<<B.b<<' '<<B.h;
        return output;
    }

 8.https://github.com/alandefreitas/moderncpp
 9.For_each loops standard-2020

 10. lamdas closure objekt anonymous function 
 int i = 7;
     [](int & v){ v *= 6; } (i);
     cout << "the correct value is: " << i << endl;

     int j = 7;
     [](int & v, int j){ v *= j; } (j,6);
     cout << "j: " << j << endl;