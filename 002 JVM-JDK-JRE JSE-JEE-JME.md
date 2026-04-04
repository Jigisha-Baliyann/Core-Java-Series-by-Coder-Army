## JVM, JRE & JDK

(Source Code) ----Compiler----> (Byte Code) ----JVM@Platform----> (Machine Code)

JVM (Java Virtual Machine) << JRE (Java Runtime Environment) << JDK (Java Development Kit)

# JVM (Java Virtual Machine)

Two types of tranlators : 
1. Compiler -> takes a Source Code, read it whole at once, then generate the whole Machine Code at once then run it on a System./Platform.
2. Interpreter -> takes a Source Code, read one line and generate its Machine Code and the System/Platform runs it, then take another line and again same, therefore it convert code line by line.

- JVM converts the Byte Code into Machine Code using Interpreter + JIT Compiler.
- JVM is a virtual machine or environment where the Byte Code is run.
- JVM also provides Security by Sandbox-model, by monitoring that the Byte Code is not requesting any un-requested access.
- JVM also brings Garbage Collection.

Java is both compiler and interpreted language. First it uses a compiler to convert Source Code to Byte Code then it uses an interpreter to convert Byte Code to Machine Code line by line.
This was due to earlier time problems : 
1. Slow Hardware
2. Limited RAMs
3. Slow Disc

- In recent times, since these problems doesn't exist anymore, we joined a JIT (Just In Time) Compiler also along with the Interpreter in Java to convert the Byte Code into Machine Code nowadays.
- The problem is that the compiler is still slow, so we use a hybrid model of both.
- The JVM uses a very smart technique for this, it reads the Byte Code and see which part of the code will be used very frequently and compiles it using JIT compiler, and the Interpreter converts the less important code line-by-line to Machine Code and run it on the System/Platform.
- In comparison, Java program takes a little longer time to compile than C/C++ but once it compiles it gives a lot of advantages.

# JRE (Java Run-time Environment)

JRE = JVM + Class Libraries ==> min. required to run a Java program

Class Libraries : the operations which a programming language performs and the methods which the program uses.

# JDK (Java Development Kit)

JDK = JRE + Compiler(Source Code --> Byte Code) + De-bugger + JavaDocs ==> complete package to run Java program

Install latest JDK from directly Oracle and do set-up and make your device Java-ready!

## JSE, JEE & JME

- JSE (Java Standard Edition) == Core Java
- JEE (Java Entriprise Edition) or JaKartaEE == for making Websites & WebApps + SpringBoot
- JME (Java Micro Edition) == a light-weight edition of Java --> obselete nowadays and replaced by Android

## First Java Code

- Text Editor or any IDE like VS Code or Intellij
- write first code in file "Demo.java"
- run command "javac Demo.java" to compile the Course Code File
- it then creates the Byte Code file as "Demo.class"
- then run the file by "java Demo.java" it will be done by (JVM + Class_Libraries) or JRE and converts into Machine Code which we cannot see then it will be run by CPU/Processor and it will give us the output which we can see on the screen.

File Name == Demo.java
'''
public class Demo {
    public static void main(String args[]) {
        System.out.println("Hello World!");
    }
}
'''
- Save it and run command "javac Demo.java" to compile this Source Code file.
- Then it generates a new Byte Code File as "Demo.class" at the same location.
- Then run command "java Demo.java" then JVM converts it to Machine Code and CPU processes it and produces the following output.
'''
Hello World!
'''
