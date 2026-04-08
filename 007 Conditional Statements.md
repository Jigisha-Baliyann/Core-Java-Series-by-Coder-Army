# Flow of Control

- Selection : "if" statements, "if...else" ladder, "switch" statements
- Iteration : "for", "while" and "do...while" loops
-   Jumps   : "break", "continue" and "pass"

# Conditional Statements in Java

## (1) Selection Statements

- Selection statements are used to make choices in the flow of control.

### IF Conditional Statements

- "if" statement
- "if...else" statement
- nested "if"s statement
- "if...else if...else" ladder

<img width="428" height="454" alt="image" src="https://github.com/user-attachments/assets/fe0a2329-4606-4a4c-bb73-1e93c52eb310" />

### SWITCH Conditional Statement

- "switch" statement is more optimized than "if" statements.
- Limited use case : the expression within "switch" statement should be evaluated to only "byte", "short", "int", "char" data types and Enumeration.
- No duplicate cases allowed in "switch" statements.
- After JDK-7, "Strings" can also be used in "switch" expressions.
- After JDK-14, "switch" statement is enhanced too much, this will be discussed later.

<img width="440" height="386" alt="image" src="https://github.com/user-attachments/assets/9101e658-2958-4d9f-a3ae-60cc615366ee" />

### SWITCH vs. IF...ELSE IF... Ladder

- "switch" statement can also do equality test whereas the "if" statements can also evaluate boolean expressions other than equality.
- "switch" is more efficient than "if...else if..." ladder because JVM make Dense Jump tables in "switch" which does only 1 evaluation, whereas "if" evaluates all conditions till it reaches desired one. Here TC is O(1).
- These Jump Tables are not always efficient. This can in such case where values inside "switch" are very Sparse away from each other. In this situation the JVM makes a Look-up Switch and works like a Binary Search internally. Here TC is O(N).
- "switch" statements can also be nested likewise.

## (2) Iteration 

## (3) Jump Statements
