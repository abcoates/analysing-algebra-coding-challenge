# analysing-algebra-coding-challenge
A coding challenge around implementing a command-line RPN calculator, and then converting algebraic expressions into RPN format for calculation.

## Core Challenge
Reverse Polish Notation (RPN) is a way of encoding algebra that was made most famous by HP (Hewlett Packard as was) calculators.  For the purposes of this challenge, an RPN expression is a set of lines of text containing whitespace-separated tokens.  The tokens can be either a decimal number or one of the four arithmetic operators '+' (plus), '-' (minus), '*' (times or multiplied by) or '/' (divided by).

When the token is a decimal number, it is pushed onto a stack.  When the token is an arithmetic, the two most recent entries on the stack are removed from the stack, the operator is applied to them, and then the result is pushed onto the stack.

When a new line is encountered, or when the end of the last line is encountered, the contents of the stack should be printed out, from oldest entry to newest.

Implement a command-line RPN calculator as described above.

### Examples
* ```"3 5"``` is printed out as: ```3 5```
* ```"2.2 3.3 +"``` is printed out as: ```5.5```
* ```"2 -5 -"``` is printed out as: ```7```
* ```"8 6 + 4 *"``` is printed out as: ```56```
* ```"3 5 + 3 1 + *"``` is printed out as: ```32```
* ```"9 9 + 3 /"``` is printed out as: ```6```
* ```"5 2 /"``` is printed out as: ```2.5```

It is an error if there are fewer than two numbers in the stack when an arithmetic operator is encountered, and it is an error to divide by zero.

## Stretch Challenge
The more common way to write arithmetic expressions is with numbers, operators and also parentheses, e.g.
* (2+3) * (4*5)
* (10/5)*5
* 10/(5*5)

Write a command-line converter that converts arbitrary arithmetic expressions into RPN expressions.