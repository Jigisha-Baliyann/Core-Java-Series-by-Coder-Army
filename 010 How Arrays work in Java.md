# Primitive and Non-Primitive Data Types in Java

Primitive Data Types : 
- int
- char
- long
- short
- byte
- boolean
- float
- double
- All the Primitive data types goes into the STACK MEMORY.
- If we write a statement " int x = 4; " then it means that ' x directly holds the value 4 '.

Non-Primitive Data Types : 
- Arrays
- Strings
- 
- All the Non-Primitive data types are stored in the HEAP MEMORY and the variable of these data types are called Reference Variables which do not keep values themselves but point to the values in memory.

# Random Access Memory in Java

- Arrays provide Random Memory Access in Java because it is stored in contiguous memory locations.

<img width="537" height="255" alt="image" src="https://github.com/user-attachments/assets/93aa54cc-9799-4588-ba73-a6fc8694043a" />

- In the above image, "arr" does not directly holds the array, it is a reference to an array.
- The below image shows the memory addresses in an integer array, since an integer is stored in 4 bytes.

<img width="302" height="128" alt="image" src="https://github.com/user-attachments/assets/7742c267-e7db-4dcf-a53f-be8c2ec99043" />

To find any element arr[i] we can write a formula as : 
<img width="512" height="83" alt="image" src="https://github.com/user-attachments/assets/854d2008-0244-4315-9acc-d41a22024b6d" />

where, Base Address is the starting address of the array, which is pointed/stored by the Reference Variable
and, D.T. represents the Data Type size (4 bytes in case of integer)

# Booleans in Memory

- According to officia Java docs, Boolean has no fix size, it depends on the JVMs according to respective platforms.
- HotSpot(Oracle) and OpenJDK has 1 Byte for Boolean as standard.
- Though we can store Boolean in 1-bit as 0/1 also, many JVMs represent Booleans in 1 Byte for Better CPU Optimization (since CPU always fetch instructions in bytes only and not bits).

# ArrayIndexOutOfBound Exception

<img width="537" height="146" alt="image" src="https://github.com/user-attachments/assets/853d4afd-af80-48f5-b4aa-dc115fc1e633" />

- In order to prevent reading/fetching random memory address.

# 2-D Arrays in Memory (Array of Arrays)

- If we write " int[][] arr = new int[3][4]; " then we have an array of size=3, where each element is itself an array of size=4.

<img width="572" height="215" alt="image" src="https://github.com/user-attachments/assets/3104add7-6f29-4e16-b418-61037bfb0ad3" />

<img width="598" height="232" alt="image" src="https://github.com/user-attachments/assets/767f19b0-9840-4270-a224-cec7cc094c1f" />






