# Arrays in Java

- Array is a static/fixed-size collection of values of similar data type.
- Arrays are defined as : datatype[] array_name = new datatype[size] ;
- "new" is a keyword which allocates Contiguous Memory in Heap.
- each allocated memory is of the same size as that of the defined datatype.
- values are inserted into Arrays as : arrayName[index] = newValue;
- indices (plural of index) are the numbered addresses in any data structure starting from 0 to (n-1) where 'n' is the size of the data structure..
- values from array are retrieved also with the help of arrays as : System.out.println(arrayName[index]);
- values in/from an array can also be inserted/retrieved with help of loops.
- ArrayName.length ==> gives the current size of this array

<img width="424" height="368" alt="image" src="https://github.com/user-attachments/assets/dd9ec061-b92d-49b1-b8ea-b98102268fcb" />

<img width="517" height="155" alt="image" src="https://github.com/user-attachments/assets/7fcbf133-c8e7-4778-b686-fbbf047ca25f" />

<img width="323" height="185" alt="image" src="https://github.com/user-attachments/assets/af5da680-3b3e-497f-ac07-589c4d5b37ee" />

# Multi-Dimensional Arrays in Java

## Conceptual Represetation of 2-D Arrays in Java

- 2-D arrays are defined as : int[][] marks = new int[3][3]; ==> which means a 3x3 matrix, where first size is the no. of rows and second size is the no. of columns in the matrix.

<img width="932" height="532" alt="image" src="https://github.com/user-attachments/assets/8657ad88-548e-46e8-a029-3da4447c78f7" />

## Logical Representation of 2-D Arrays in Java in Memory

- The computer does not have any concept of Rows or Cloumns like we humans visualize, but it only has the concept of Contiguous Memory Location.

<img width="1398" height="795" alt="image" src="https://github.com/user-attachments/assets/8671f988-3ef1-4047-99cd-3f380212869f" />

<img width="683" height="343" alt="image" src="https://github.com/user-attachments/assets/16ca9e5b-3055-4965-88b1-7409f0c154ad" />

## 3-D and above Dimensional Arrays

<img width="739" height="327" alt="image" src="https://github.com/user-attachments/assets/b0070c64-3111-4cb9-a4f7-d8d374d83d50" />

## Defining Arrays along with Declaration in Java

<img width="504" height="314" alt="image" src="https://github.com/user-attachments/assets/0207ccde-5b47-4412-a7f7-3cd60ac2e40b" />

## Multi-Dimentional Arrays in Code

<img width="838" height="715" alt="image" src="https://github.com/user-attachments/assets/8cbded5c-a7e5-4c29-88b2-7cfd0ec8641f" />

<img width="832" height="609" alt="image" src="https://github.com/user-attachments/assets/2ca33ff7-1663-4faa-b759-dc60e4aee84d" />

# Introduction to Strings in Java

- String is also a non-primitive data type in Java.
- They are declared as : String variableName = "StringValue";
- They are always written within double quotes.

- NOTE: In System.out.println() we always put the String value to output;
- Concatenation is done in Strings by '+' operator.

<img width="640" height="354" alt="image" src="https://github.com/user-attachments/assets/daf74edf-62e0-42cd-b1e5-1dd76e1ff979" />
