# Why this is needed?

'''
public class Demo {
    public static void main(String[] args) {
        float f = 8.125f;
        System.out.printf(format: "%.20f%n",f);
        // this syntax is used to print 20 decimal places in this float/double number
    }
}
'''

But if f=0.7 then it gives output at 0.69999998807907100000 because it is how this f is stored in memory in this case.

# How Negative Numbers are stored in Memory in Java?

'''
byte a = 42; // it will be 00101010 in binary 
byte b = -42; // it is stored in memory in the form of 2's complement in java
'''

- Range of byte is -128 to +127, it uses 8-bits in memory.

## 2's Complement in Binary

- let num = 42 in decimal
- 42 in binary = 00101010
- 1's complement of num will be made by complementing it bit-wise i.e. 11010101
- 2's complement of num will be made by binary addition of 1 with its 1's complement i.e. 11010101 + 1 = 11010110
- hence -42 will be represented in binary as the 2's complement of 42 i.e. (-42)10 = (11010110)2.
- hence the memory will save 11010110 for b = -42.

## How 2's Complement is converted back to Decimal?

- the memory checks what is the MSB (most significant bit -- lefter most) in 2's complement in binary.
- if MSB = 1 then it is a negative decimal number and if MSB = 0 then it is a positive decimal number.

Compiler converts binary to negative decimal number : 
- take 1's complement of the binary stored in memory i.e. 11010110
- 1's complement of 11010110 is = 00101001
- 2's complement = 1's complement + 1 = 00101001 + 1 = 00101010
- 00101010 = 32 + 8 + 2 = -42

## Why take 2's complement and not 1's complement to handle negatives?

- to handle the case of 0.
- if someone store " byte b = -0; " then 0 = 00000000 in binary but due to negative sign it will take 1's complement as 11111111 and then 2's complement as 11111111 + 1 = 100000000 (9-bits) but only 8-bits will be stored i.e. 00000000 will be stored in memory.
- since -0 saved from compiler is saved as 00000000 in memory, it will retrieve back as 0 only.
- but this cannot be possible by only 1's complement, hence we use 2'c complement.

# How Float/Double Numbers are stored in Memory?

<img width="942" height="285" alt="image" src="https://github.com/user-attachments/assets/3e716bf9-d0a6-47ab-a99e-03d9f8adedd6" />

1. for storing f = 8.125 into memory, we have to convert it completely into binary :
- now 8 = 1000 and 0.125 = 0.001 so it becomes f = (8.125)10 = (1000.001)2
2. now make it into the form of (1.xx) * 2^exp.
- so f = (1000.001)2 = (1.000001 * 2^3)2 in binary
3. add Bias to the exponent now : (for float, bias = 127)
- 3 + 127 = (130)10 = (10000010)2
4. put/place values back in the memory :
- number becomes ==> 1.000001 * 2^10000010
- sign-bit = 0 (for positive)
- exponent = 10000010 (8-bits)
- mantissa = 00000100000000000000000 (23-bits)

<img width="1035" height="250" alt="image" src="https://github.com/user-attachments/assets/30d427c5-4624-4480-b1fc-c34915a95969" />

# How Float/Double Numbers are retrieved back from Memory (binary to decimal) ?

Decimal = (-1)^sign * (1 + Mantissa) * 2^(exp. - Bias)

= (-1)^0 * (1 + Mantissa) * 2^(10000010 - 127)
= 1 * (1 + .000001) * 2^(130 - 127)
= 1 * (1 + 2^-6) * 2^3
= 1 * (1 + 1/64) * 8
= 8 * (1 + 0.015625)
= 8 * 1.015625
= (8.125)10

# Why f=0.7f gives problem ? 

1. Express into binary
   (0.7)10 = (0.101100110(0110....infinite))2
2. Represent into 1.xx * 2^exp.
   ==> 1.01100110.... * 2^-1
3. Add Bias to make Exponent
   ==> (-1 + 127) = (126)10 = (01111110)2
4. Express in Memory
   sign-bit = 0
   exponent = 01111110
   mantissa = 0110_0110_0110_0110_0110_011
5. Retrieve back from Memory
   ==> (-1)^sign * (1 + Mantissa) * 2^(exp. - Bias)
   = (-1)^0 * (1 + 0.0110_0110_0110_0110_0110_011) * 2^(126 - 127)
   = 1 * (1 + 2^-2 + 2^-3 + 2^-6 + 2^-7 + 2^-10 + 2^-11 + 2^-14 + 2^-15 + 2^-18 + 2^-19 + 2^-22 + 2^-8) * 2^-1
   = (1 + 0.39999997615814208984375) * 1/2
   = 1.39999997615814208984375 * 1/2
   = (0.69999998807907104421875)10
   ~ 0.7

# The IEEE Standard Floating Point Representation

32-bit Representation --> Bias = 127 --> used for Float
This is done to make the exponent positive to store number into memory.

for exponent = 8-bits 
Bias = 2^(exp.-1) - 1 = 2^(8-1) - 1 = 2^7 - 1 = 128 - 1 = 127

<img width="949" height="241" alt="image" src="https://github.com/user-attachments/assets/0868c9c7-926c-4ba9-ab36-c0d7141a0dbe" />

64-bit Representation --> Bias = 1023 --> used for Double
for exponent = 11-bits
Bias = 2^10 - 1 = 1023

# BigDecimal -- the new concept to solve this problem
(this will be covered in further lectures)
