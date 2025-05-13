# 🏁 RaceCode Compiler

RaceCode is a custom compiler built using **Lex (Flex)** and **Yacc (Bison)** that parses and interprets a simple racing-themed programming language and generates Three Address Code for now it generates TAC for arithmetic and If/else loop statement code. It takes `.f1` files as input and processes race-style logic like starting lights, lap count, speed updates, yellow flags, and chequered flags.

---
## Rules of Language
•	lightsout: Marks the start of the program
•	chequered: Marks the end of the program
•	pitstop: Declares a variable
•	boost: Addition operator (+)
•	brake: Subtraction operator (-)
•	turbo: Multiplication operator (*)
•	slipstream: Division operator (/)
•	telemetry: Prints a variable or expression
•	sector: Begins an if statement
•	then: Separates condition from the then-block
•	else: Introduces an optional else-block
•	endsector: Ends an if statement

- Program Structure
lightsout
program content
Chequered


## 🚀 Features

- Lexical analysis using Flex
- Syntax parsing using Yacc/Bison
- Intermediate TAC (Three Address Code) generation

---

## 📂 Project Structure
- a.exe (C executable file after compiling)
- input.txt (In this the sample code would go)
- output.txt (In this the output will be seen )
- lex.l (Lexical Code)
- yacc.y (Syntax Code)
- lex.yy.c (Generated C code after flex lex.l)
- yacc.tab.h (Yacc header file)
- yacc.tab.c (Generated C code after bison -d yacc.y)


##Commands to Run Project
- Currently this project Structure consist of all the header and C file which are generated after running the commands but initially there are only input.txt, lex.l, yacc.y
- Below are the Sequence of Command:
  - bison -d yacc.y
  - flex lex.l
  - gcc lex.yy.c yacc.tab.c
  - ( after the command is ran an a.exe will be generated )
  - .\a.exe (if running in VS Code )
