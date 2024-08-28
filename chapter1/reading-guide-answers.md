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
  > ```
  > The linker is what produces the final compilation output from the object files the compiler produced. This output can be either a shared (or dynamic) library (and while the name is similar, they haven't got much in common with static libraries mentioned earlier) or an executable. It links all the object files by replacing the references to undefined symbols with the correct addresses. Each of these symbols can be defined in other object files or in libraries. If they are defined in libraries other than the standard library, you need to tell the linker about them.
  > ```
  >   ... which is quite a mouthful, so let's dissect that snippet of an explanation.
  >   So basically, builtin functions like `printf("deez nuts")` are part of a library that exists as an object file, which contains executable machine code
  2. What is the difference between a relocatable object program and an executable object program?
  3. Make a comparative table between each phase of the compilation system
   | Preprocessing | Compiling | Assembling | Linking |
   |---------------|-----------|------------|---------|
   | It only transforms a text file into another text file | It also transforms an expanded text file into a text file that contains Assembly code | It "compiles" (i.e. assembles) the file produced by compiling | It retrieves the functions that have not been "translated" by the compiler |

## 1.3
5. Describe the `switch` statement in the C Programming language and its' differences to the `if-else` statement.
6. What is overhead and what does it mean for an overhead to be incurred?
7. What is a function call and what does the question "How much
overhead is incurred by a function call?" even means?
8. Explain the differences between a `for` loop and a `while` loop, explain when you should use one over the other and why would the idea of a `while` loop being more efficient than a `for` loop make sense
9. What is a pointer reference?
10. What is an array index?
11. What is a local variable?
12. What is an argumend passed by reference?
13. What is a link-time error?
14. What is a buffer flow vulnerability?
## 1.4
15. What is a shell and which is its purpose?
16. Point out the main difference between the shell and other programs in the operating system.
17. What is a bus?
18. Make a table comparing a controller and an adapter.
19. Which are the main parts of a Processor and which are the operations of the ALU?
## 1.5
20. Make a table comparing the SRAM and the DRAM
21. How does the computer system transfers information from the I/O disk to the main memory?
## 1.7 
22. What are the two purposes of the OS?
## 1.9
23. Enunciate Amdahl's law in your own words
24. Differentiate between Parallelism and concurrency
