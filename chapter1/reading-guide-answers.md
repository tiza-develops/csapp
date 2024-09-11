# Chapter 1 Reading Guide
## 1.1
1. What are the two main parts of a computer systems and which is its main function?
> Hardware and software, which work together to run applications
2. List practical things that come with knowing how a computer system works on an internal level.
> - Avoid strange numerical errors
> - Optimize C code by exploiting the processor design
> - Avoid security holes
> - Recognize errors during linking
> - Write my own Unix shell
3. Which are the three notorious reasons for the success of C as a programming language?
> - Its relation to the ubiquitous Unix operating system
> - Its small size and relative simplicity
> - A practical design
## 1.2
4. What are the four stages of a compilation system?
> - Preprocessing
> - Compiling
> - Assembling
> - Linking
  1. What's the name of the first stage in a compilation system and what it does? What about the last?
  > - Preprocessing modifies the source code file to expand external functions and abbreviations like `#include <package>`
  > - Linking:
  >     According to R. Martinho Fernandes from Stack Overflow: 
  > > The linker is what produces the final compilation output from the object files the compiler produced. This output can be either a shared (or dynamic) library (and while the name is similar, they haven't got much in common with static libraries mentioned earlier) or an executable. It links all the object files by replacing the references to undefined symbols with the correct addresses. Each of these symbols can be defined in other object files or in libraries. If they are defined in libraries other than the standard library, you need to tell the linker about them.

  >   ... which is quite a mouthful, so let's dissect that snippet of an explanation.
  >   So basically, builtin functions like `printf("deez nuts")` are part of a library that exists as an object file, which contains executable machine code
  2. What is the difference between a relocatable object program and an executable object program?
  3. Make a comparative table between each phase of the compilation system

   > | Preprocessing | Compiling | Assembling | Linking |
   > |---------------|-----------|------------|---------|
   > | It only transforms a text file into another text file  | It also transforms an expanded text file into a text file that contains Assembly code | It assembles the file that the compiler produced | It retrieves the functions that have not been "translated" by the compile|

## 1.3
5. Describe the `switch` statement in the C Programming language and its' differences to the `if-else` statement.
> There are a way to substitute long `if-else` statements in C. So instead of:
> ```c
> if (num == 2) {
>   foobar;
> } else if (num == 3) {
>   foobar
> } else if (num == 4) {
>   foobar
> } else if (num == 5) {
>   foobar
> }
> ```
> You can instead "`switch`" over a variable like so:
> ```c
> int var = 1;
> switch (var);
> {
>   case 1:
>     foobar;
>     break;
> 
>   case 2:
>     foobar;
>     break;
> 
>   case 3:
>     foobar;
>     break;
> }
> ```
> And so on

6. What is overhead and what does it mean for an overhead to be incurred?
> It refers to the (computational) physical resources that are being used to peform a task particularly excess of it
7. What is a function call and what does the question "How much overhead is incurred by a function call?" even means?
> A function in programming is a piece of code that can be repeated, so then you invoke it by typing `name_of_the_function(argument)`. That is a function call, and according to the last answer, asking "How much overhead is incurred by a function call?" is the same as to say. "How much of an excess of computational resources are used when you invoke a function?"
8. Explain the differences between a `for` loop and a `while` loop, explain when you should use one over the other and why would the idea of a `while` loop being more efficient than a `for` loop make sense
9. What is a pointer reference?
> Pointers and references are actually two very different thing in the C programming language. A pointer is a slot in memory that references the memory slot of the variable that has been assigned to it. A reference, however, does not has any space in memory, is at best, an alias to the **variable**, not its value. A pointer reference is then a variable that aliases a pointer.
10. What is an array index?
> The number of position of a data structure that is like a pile of plates, array indexes always start with 0
11. What is a local variable?
> A variable that only makes sense in the program inside its particular function.
12. What is an argument passed by reference?
> You remember what is a reference from question 9, right? Of course you do, you are a smart person. Well, imagine now you have a `int function name()` and you want to input your variable `char crazy_variable` into it. You could `function(crazy_variable)` or you could make a reference variable to `crazy_variable` and input that instead. Congratulations! you just passed an argument by reference
13. What is a link-time error?
> when object code file X was being made I was told variable/function/etc. Y would be defined in another object code file or in a library but it doesn’t actually exist!
14. What is a buffer overflow vulnerability?
> First we gotta understand what a buffer is. So, the computers store information in bytes and words, so basically a program or application can say "I will use this many words for a specific purpose, so I call dibs on this many words in this part of the main memory". That is a buffer, and it, obviously, has a limited memory
> Imagine now that said buffer is receiving more information (bytes) that expected, then the information will be alocated in adjacent memory slots. 
## 1.4
15. What is a shell and which is its purpose?
> A persistent process (more on that later) that exposes the Operating System for the user and the applications. Mainly for the purpose of abstracting away the hassle of interacting directly with main memory adresses and device drivers.
16. Point out the main difference between the shell and other programs in the operating system.
> The shell manages basic computer tasks and duties, that other programs rely on. So the shell is more fundamental
17. What is a bus?
> The system that transfers information between different computer components
18. Make a table comparing a controller and an adapter.
> A controller is hardwired into the computer motherboard and the adapter is inserted into a slot
19. Which are the main parts of a Processor and which are the operations of the ALU?
> The processor is composed of three parts:
> - Arithmetic-Logic Unit
> - Control Unit
> - Registers
The Arithmetic-Logic Unit (ALU) has three categories of functions:
> - Arithmetic operations: dealing with integers
>  - Adding
>  - Substracting
>  - Add 1 to a number
>  - Substract 1 to a number
>  - Substract from 0
> - Bitwise operations: take two bit strings, and replacing one of them
>   - NOT: shifting the value of each bit in the string
>   - AND: reads each bit of both strings, if both are 1, it returns 1, and 0 otherwise.
>   - OR: returns 1 if either is 1
>   - XOR: returns 1 iff exactly one of the bits of the string is 1, same with 0
> - Bitshift operations
>   - Bit adressing
>   - Arithmetic shift
>   - Logical Shift
>   - Circular Shift
## 1.5
20. Make a table comparing the SRAM and the DRAM

| SRAM | DRAM |
|------|------|
| It stores information as long as there is power available | It can store information for a few miliseconds when there is no power available |
| It uses transistors | It uses capacitors |
| No refreshing of memory is required | It needs to refresh memory constantly |
| High access speeds | Low access speeds |
| Cache Memory | Main Memory |
21. How does the computer system transfers information from the I/O disk to the main memory?
> Through a bus
## 1.7 
22. What are the two purposes of the OS?
## 1.9
23. enunciate amdahl's law in your own words
24. 
25. differentiate between parallelism and concurrency
