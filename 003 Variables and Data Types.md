# Variables, Identifiers, Literals, Comments & Keywords

- "Variables" are the containers which hold some value in the memory.
- "Identifiers" are the representations of containers/variables.
- "Literals" are the values which are stored into containers in memory.

- "Comments" are ignored by the compiler, these are used for
- Single line comments starts with //.
- Multiple line comments are enclosed within /* and */.

- "Keywords" are the reserved words by the programming language, which cannot be used as literals.
- Java has total 68 Keywords.
- 'goto' and 'const' are special Keywords in Java which are not defined in the language and used anywhere, but only kept reserved.

# Data Types

- The type of value stored in an Identifier.
- Java is a statically-typed language i.e. we have to declare the type of variable at the time of its initialization or declaration.
- Types of Data types on Java :
1. Primitive Data Types :
   o Integer ==> byte, short, int, long
   o Real Number ==> float, double
   o Character ==> char
   o Boolean ==> boolean
2. Non-primitive Data Types

# Integer Data Types

Different data types have different range.
byte << short << int << long
- "byte"  (width-8)  : -128 to 127
- "short" (width-16) : -32,768 to 32,767
- "int"   (width-32) : -2,147,483,648 to 2,147,483,647
- "long"  (width-64) : -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807

- Every number is Signed in Java.

## Real Number Data Types

- "float"  (width-32) : 1.4 * 10^-045 to 3.4 * 10^038 ==> Single Precision
- float f = 10.54f;
- "double" (width-64) : 4.9 * 10^-324 to 1.8 * 10^308 ==> Double Precision
- double d = 6.022e23; // 6.022 * 10^23 ==> 6.022E23 as Output in Scientific Form
- "double" is always preferred for latest processors and we don't use "float" in real-life projects.

## Character Data Type

- "char" --> can represent unicode characters
- Characters are represented within single quotations ''.
- Previously English characters were assigned ASCII codes (which has range 0 to 127 or 8-bits) like 65='a'.
- Java introduced Unicodes (16-bits) to represent all characters over the world into numeric/integer codes/values.

## Boolean Data Type

- "boolean" stores only two types of values : "true" or "false".

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e616726b-4567-4580-9c1f-1b0d03974a37" />

## Important/Note

- "float", "double" and "long" data types can also be made more readable by adding _ (underscores) which will be ignore by the compiler.
- "float" and "double" cannot take _ immediately adjacent to the _ otherwise it will give error.

- int x; // only declared, can be defined later by user input.

# Number Systems

- Binary       : base-2             : byte b = 0b101; ==> b = 5 (decimal output)
- Octal        : base-8             : byte b = 05;    ==> b = 5 (decimal output)
- Decimal      : base-10 (default)
- Hexa-decimal : base-16            : byte b = 0xA;  ==> b = 10 (decimal output)
