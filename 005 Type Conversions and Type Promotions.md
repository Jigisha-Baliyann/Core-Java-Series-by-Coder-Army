# Type Conversion in Java

1. Implicit Conversion (done by Java automatically)
2. Explicit Conversion (done by programmer forcefully)
3. Truncating Conversion

## Rules of Implicit Conversion : 

- Destination Data Type should be wider than Source Data Type.
- byte (8-bits) < short < int (32-bits) < long 
- This is also called as Widening Conversion.
- "char" (16-bits) can also be converted to "int" (32-bits).

## Explicit Conversion : 

- To be done manually/forcefully with the help of Casting.
- This is also called as Narrowing Conversion.

'''
int i = 300;
byte b;
b= i; // this will give error.
b = (byte)i; // this is casting here.
System.out.println(b); 
'''

For output of above,
(300)10 = (100101100)2 --> 9-bits
        = 00000000_00000000_00000001_00101100 as "int" data type
After casting into only 8-bits "byte" data type, b = (00101100)2 = (44)10
Hence, in type casting, the data is truncated.

## Truncating Conversion : 

'''
float f = 16.25f;
int i;
i = f; // this will give an error.
i = (int) f; // this will make i=16
'''

This is called Truncating Conversion because it truncates the decimal parts of "float" and "double".

## Boolean to any Data Type Conversion : 

- This type of conversion is not possible because Boolean is a special type of Data Type.

# Type Promotions in Java 

'''
byte b = 50;
b = b*2;
'''

This will internally promote b in "b = b*2" to integer and the result become 100 which gives error, hence type casting need to be used here as follows.

'''
byte b = 50;
b = (byte)(b*2);
'''

## Rules of Type Promotions : 

- any "byte", "short" and "char" values are promoted to "int".
- if one operand is "long", then the whole expression will become "long".
- if one operand is "float", then entire expression will become "float".
- if one operand is "double", then entire expression will become "double".


