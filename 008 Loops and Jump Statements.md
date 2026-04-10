# Iterations & Loops in Java

- "while" loop
- "do...while" loop
- "for" loop
- "for...each" loop --> will be discussed in Arrays and later
- nested loops

## (1) "while" loop

(initialization)
while (end expression/condition) {
    // statements of action
    // upgradation
}

- a "while" loop can behave like an infinite loop if we don't include the 'upgradation' statement inside it.
- it is an Entry-Control loop.

## (2) "do...while" loop

(initialization)
do {
    // statements of action
    // upgradation
} while (end condition/expression) ;

- it is an Exit-Controlled loop.
- it is used to execute the loop block at least once, despite the condition.
- it is used in Menu item selection use-case.

## (3) "for" loop

for (initialization ; end condition ; upgradation) {
    // statements of action
}

Flow of control of "for" loop : 
1. First assignment statement is executed i.e. Variable definition.
2. Then 2nd condition statement is evaluated to True / False.
3. If True, control flow will evaluate the body of the loop.
4. Once loop body is finished, control flow will go back to the "for" statement, and 3rd increment statement will be evaluated.
5. Again, conditional statement is eveluated.
6. Repeat 2-5.
7. If condition at 2 is False, it exits the loop.

### "for" loop with multiple literals & conditions

<img width="753" height="543" alt="image" src="https://github.com/user-attachments/assets/6d9f6457-27fa-4fb9-8530-f9f8159a1a1f" />

## (4) Nested Loop

<img width="313" height="307" alt="image" src="https://github.com/user-attachments/assets/4d51b268-912e-4b16-9f4b-e4e4739897ea" />

# Jump Statements in Java

## "break" Jump Statement

<img width="496" height="338" alt="image" src="https://github.com/user-attachments/assets/a1abad2f-0f05-4271-b581-b30a25e83cc8" />

## "continue" Jump Statement

<img width="244" height="184" alt="image" src="https://github.com/user-attachments/assets/8b141c2f-7388-4e79-8756-c3c2a08dc2ee" />

# Jump Statements inside Loops

<img width="530" height="660" alt="image" src="https://github.com/user-attachments/assets/52a4519b-14c4-4866-812c-3488c804b16d" />

# Labels in Java

- In Java, we can also give names to the loops for identifying them to label directly.

<img width="371" height="473" alt="image" src="https://github.com/user-attachments/assets/61a63330-a149-49b6-9d03-0accb5863f31" />

# Code Blocks in Java

<img width="666" height="309" alt="image" src="https://github.com/user-attachments/assets/4cf2e556-85a1-4dbd-bd2a-158b2fa57449" />
