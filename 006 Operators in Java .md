# Operators in Java

1. Arithmetic / Mathematical Operators
2. Relational Operators
3. Bitwise Operators
4. Bitwise Shift Operators
5. Logical Operators
6. Assignment Operator
7. Ternary Operator

## (1) Arithmetic / Mathematical Operators

- + : addition operator
- - : subtraction operator
- * : multiplication operator
- / : division operator
- % : modulus/remainder operator

<img width="1350" height="857" alt="image" src="https://github.com/user-attachments/assets/72f403e2-2f12-4339-be22-259c4eabb836" />

In some programming languages including Java, two operators can be combined together like += , -= , *= , /= , %= which are called as Assignment Operators.

<img width="693" height="477" alt="image" src="https://github.com/user-attachments/assets/dcf366a9-d049-4c9e-b16b-7cdf451f9de4" />

- ++ : increment operator
- -- : decrement operator

<img width="499" height="149" alt="image" src="https://github.com/user-attachments/assets/89ad01ec-a6a3-4541-a245-6b4ed67ea80b" />

### Pre- & Post- Increment/Decrement Operators

- Pre-  : it means first the value will be updated and then it will be assigned/used.
- Post- : it means that first the old value will be assigned/used and then it will be updated.

<img width="756" height="519" alt="image" src="https://github.com/user-attachments/assets/a7b8aa3a-548f-433b-a53e-8dd69ed8af9b" />

## (2) Relational Operators

- == : is equal to
- != : is not equal to
-  < : is lesser than 
-  > : is greater than
- <= : is less than or euqal to
- >= : is greater than or equal to

- These opreators evaluate the expression result to Boolean value either True or False.

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b3bae71c-3451-42ea-82fc-99964749e8da" />

<img width="521" height="324" alt="image" src="https://github.com/user-attachments/assets/469c09a0-3de3-4768-98cf-faf83a5db219" />

<img width="492" height="530" alt="image" src="https://github.com/user-attachments/assets/c8b56b13-efe3-41cf-8e74-524acec1f8cf" />

## (3) Bitwise Operators

- ~ is a Unary Bitwise operator while all others are Binary Bitwise operators.

- & : Bitwise And operator
- | : Bitwise Or (Inclusive) operator
- ^ : Bitwise Exclusive Or operator
- ~ : Bitwise Complement operator
 
<img width="678" height="228" alt="image" src="https://github.com/user-attachments/assets/6a5be2f5-44fe-4e3f-b539-86026c620118" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/9bd5bfe3-9830-4b8e-b8d4-682bec5589ac" />

## (4) Bitwise Shift Operators
 
- >>  : Shift Right operator
- <<  : Shift Left operator
- >>> : Shift Right with Zeroes operator

1. Left Shift Operator

<img width="738" height="214" alt="image" src="https://github.com/user-attachments/assets/7b397886-6ced-471f-9bae-e73bb4069569" />

- In general : b << N === b * 2^N

<img width="738" height="367" alt="image" src="https://github.com/user-attachments/assets/2fdddd3f-09bd-4a7f-9cf2-706f38d3b632" />

- These operations can be done only on "int" and "long" data types and not on "byte" or "short".
- If Shift Operations are put on "byte" or "short" data types then they will be Type Promoted to "int" and then operated upon, and any "int" data type also Type Promotes to "long" data type in case when its bit-range is full.

<img width="780" height="335" alt="image" src="https://github.com/user-attachments/assets/153c2a57-54bb-4ba5-a141-08d1bb160380" />

<img width="799" height="292" alt="image" src="https://github.com/user-attachments/assets/411ca7cc-9555-4448-8394-69d3847b1c85" />

<img width="587" height="348" alt="image" src="https://github.com/user-attachments/assets/d35768ba-634c-4436-82d3-57d7629868a9" />

2. Right Shift Operator

<img width="739" height="324" alt="image" src="https://github.com/user-attachments/assets/cc4778f4-9ac4-4829-a28b-67dffcc04d15" />

- In general : b >> N === b * 2^-N
- LSB is lost at every Right Shift operation, and no problem like Left Shift operation.
- It introduces the same bit at new MSB which is the previous MSB before shift operation.

<img width="693" height="218" alt="image" src="https://github.com/user-attachments/assets/42c84787-3c9b-423e-9501-ef2163bd0e85" />

3. Right Shift with Zeroes

- It is a dumb shift which always introduces a 0 as MSB in a Right Shift operation.
- it is used in those cases where we always need positive numbers only for consideration.

- &= , |= , ^= , >>= : , <<= , >>>= can also do bitwise operations and then assign value.

## (5) Logical Operators

- These operators work on expressions and eveluate the result as either True or False.
- && : Logical And Operator
- || : Logical Or Operator
-  ! : Logical Not/Compliment Operator

<img width="283" height="155" alt="image" src="https://github.com/user-attachments/assets/91ef9b2f-0eb2-47d1-ba99-fc7438953c7e" />

### Short Circuit Condition

- In the expression 'A && B', if condition A is False then condition B is not checked and it produces result as False.
- In the expression 'A || B', if the condition A is True then condition B is not checked and it produces result as  True.
- Both these cases are called Short Circuits for Logical Operators.

- We can use Bitwise operators & and | in place of Logical operators && and || respectively to prevent Short Circuit conditions and it will also do same work for expressions. (This is a very smart interview question.)
- This is used in such cases where we need to increase the condition in some conditional statements.

## (6) Assignment Operator

- The = is the assignment operator.
- int a = 5;
  int b = 10;
  a = b; // it assigns value of b into a --> this is assignment.

- We can also make a chain of assignment operators in Java as :
  int a = b = c = 10;

## (7) Ternary Operator ( ? : )

- This is a special operator which operates on 3 operands.
- This is used in conditionals, and will be covered in that part later.

# Precedence of Operators in Java

- Brackets () have highest precedence for operators.

<img width="924" height="612" alt="image" src="https://github.com/user-attachments/assets/95f3a98d-dbe7-4871-bffd-fb58c2261cd5" />
