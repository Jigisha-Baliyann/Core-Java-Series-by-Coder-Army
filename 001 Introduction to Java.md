## C/C++ --> 1980s-90s

- Fast
- Simple
- Low-level language (close to Hardware & not much Abstraction layers)

## Problems in C/C++

- C/C++ were not Portable.
- Compiler is a software which converts any language/code into Machine/Binary code which is only understood by the machine.
- The compiler and the C/C++ languages both are Platform-oriented/dependent.
- For every different Platform, a C/C++ code need to compiled separately to run because different Platforms have different Machine Codes.
- Platform = Processor + Operating System
- E.g. P-1    Intelx86 +  Windows
- E.g. P-2      ARM    +   MAC
- When a C/C++ code is compiled using a Compiler then it converts it into Machine Code. It sends command to OS for displayign anything to console, memmory allocation, file operations etc. At back-end, when the C/C++ code is compiled then the OS sends its System-Libraries in compiled form to perform these actions, which is included in the Machine code. Hence, for same C/C++ code compiled on different OS, their system libraries are also different, hence their Machine Codes are also different.
- ISA (Instruction Set Architecture) is an interface between the Program and the Processor which tells the Processor various commands like ADD, LOAD, STORE, JUMP etc. ISA acts like the Grammar for a Processor.
- The Processors (CPUs) consists of billions and trillions of Transistors (which has two states of current : ON-1 and OFF-0). Different processors may have different configurations of their Electrical Pins at Hardware level. So different Processors also have different ISAs/grammars. Hence same C/C++ code will convert into different Machine Codes for different Processors.

## Why Java was needed?

1. C/C++ were platform-dependent languages.
2. They are not very simple, included some complex comcepts like Pointers, Multiple inheritance, Manual Memory Allocation & Deallocation.
3. They were not secure.

## Features of Java

1. PORTABLE
- Java introduced the concept of Byte Code to become Portable.
- Java Compiler converts the "File.java" Source Code into "File.class" Byte Code which is Independent for all Platforms.
- JVM (Java Virtual Machine) is a software which converts Byte Code into Machine Code for different Platforms accordingly.
- This is how Java is Portable / Platform-independent / WORA (Write once Run anywhere).
- Note that the JVMs are platform-dependent.

2. SIMPLE
- C/C++ included some concepts like Pointers, Multiple inheritance, Manual Memory Allocation & Deallocation.
- Java removed all these complex concepts of C/C++ and hence became Simpler.

3. SECURE
- Since Java is platform-independent, so developers used it on Back-end then Java Servelet came into existance.
- Java Applets also came into existance to make initial Front-end which can run on browsers. From JDK 10/11, Applets were discontinued.
- Considering the massive use-cases of Java, there was also a concern for its security. So Java Security was also introduced which is done by JVM which runs the Byte Code in a secured environment to prevent system. This is also called Sand-box model of Java.
- Thus using JVM and Sand-box, Java also provided security.

(We will learn about JDK in further lectures.)

## Why then C/C++ were not made Platform-Independent by introducing the concepts of Byte Code and JVM-like software ??

- Microsoft did this experiment with C# and made it also platform-independent, also it is a close cousin to C/C++.
- But this was not done with C/C++ because we didn't want to see it as platform-independent, we want it to keep close to hardware only and run fast.
- All the languages which came after Java implemented the concept of platform-independence like C# and Python, but implements it slightly differently.
