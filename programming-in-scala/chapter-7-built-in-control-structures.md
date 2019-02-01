# Chapter 7. Built-in Control Structures

Scala has only a handful of built-in control structures. The only control structures are if, while, for, try, match, and function calls. The reason Scala has so few is that it has included function literals since its inception. Instead of accumulating one higher-level control structure after another in the base syntax. Scala accumulates them in libraries. Chapter 9. will show precisely how that is done. This chapter will show those few control structures that are built in.

One thing you will notice is that almost all Scala's control structures result in some value. 
- This is the approach taken by functional languages, in which programs are viewed as computing a value, thus the components of a program should also compute values. 
- In imperative languages, function calls can return a value, even though having the called function update an output variable passed as an argument would work as well. In addition, imperative languages often have a ternary operator (such as the ?: operator of C, C++ and Java), which behaves exactly like if, but results in a value. Scala adopts this ternary operator model, but calls it if. In other wrods, Scala's if can results in a value. Scala then continues this trend by having for, try and match also results in value.

Programmers can use these result values to simplify their code, just as they use return values of functions. Without this facility, the programmer must create temporary varibales just to hold results that are calculated inside a control structure. Removing these temporary variables makes the code a little simpler, and it also prevents many bugs where you set the variable in one branch but forget to set it in another.

Overall, Scala's basic control structures, minimal as they are, are sufficient to provide all of the essentials from imperative languages. Further, they allow you to shorten your code by consistently having result values. To show you how all of this works, this chapter takes a closer look at each of Scala's basic control structures.

## 7.1 IF EXPRESSIONS
