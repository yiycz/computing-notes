---
tags:
  - modularisation
  - theory
---
# Modular Programming 

A module can be defined as a section of an algorithm that can be reused and that is dedicated to performing a single function. 

- Each module performs a distinct function and has a clearly defined interface for communication with other modules.
- Modules are usually implemented as functions, classes, or separate files
- Promotes reusability, maintainability, readability, and collaboration in software development

### Key Features:

- Decomposition → The program is broken down into smaller, logical parts (modules)
- Encapsulation → Each module hides its internal details and exposes only what is necessary (its interface)
- Independence → Modules can be developed and tested separately
- Reusability → A module can be reused in different programs
- Maintainability → Easier to update/debug a specific part of the program without affecting others


### Benefits of using modular programming

- Allow the subroutine to be called from many / multiple places
- May be (independently) tested and debugged
- Reduce unnecessary duplication / programme lines



# Functions and Procedures

A procedure is a block of program code statements designed to carry out a definable task.

A function is a block of program code statements that returns a single value to the program that called it. 

### Difference between procedure and function

- A function only accepts input parameters (pass by values) whereas a procedure accepts input or output parameters (pass by reference)
- A procedure is a bundle of code, it does not have return type whereas function has return type. 
- Hence a function may return a value for its input parameters whereas a procedure may not return a value for its input parameters. 


### Passing parameters by value and by reference

- By value: the actual value is passed into the procedure
- By reference: the address of the variable is passed into the procedure 



### Difference between global variables and local variables 

A global variable exists throughout the entire programme, while a local variable only exists in the subroutine in which it is declared.

A global variable is a longstanding variable accessible anywhere throughout the main program and all subroutines, and the scope of a local variable is only accessible within the function/procedure in which it is declared in. 










