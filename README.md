# Java Interview 
This repository is designed to help you to face Java interviews with confidence.

## Top Tricky interview Questions on core java
video - https://www.youtube.com/watch?v=PwiuAebCruY

1. Why Java is not 100% Object-oriented?
* Because there are primitive data types like
    *  boolean
    *  byte
    *  char
    *  int
    *  float
    *  double
    *  long
    *  short
        
* To make them OO we have wrapper classes that actually "wrap" the primitive data type into an object of that class.
--------------------
2. Why pointers are not allowed in Java?

* Unsafe
* Increase the complexity
* Since JVM is responsible for implicit memory allocation, there is no need to use pointers.
-----------------------

3. What is JIT compiler in Java?

JIT - Just In Time Compilar

* JDK includes Javac.exe compiler that converts Java code to byte code.
* Then byte code goes into the JRE. It contains (Interpreter + JIT Compiler)
* (Interpreter + JIT Compiler) converts Byte Code to Machine Code (Machine independent code).
* Interpreter goes line by line. (It decreases efficiency)
* JIT optimizes the performance in Run time.
* JIT compiles a bunch of code without interpreting.
-----------------------

4. Why String is immutable in Java?

immutable = you cannot modify once the object is created.

* String to be immutable otherwise shared reference can be changed from anywhere.
* Security purposes - string is shared on different areas like file system, networking connection, DB connection.
* It secures since no one can change the reference of String once it gets created.
* Even if anybody tries to change the data in the String, the new String is created and not considered the same as the previous one. 
-------------------------

5. What is a marker interface?

* marker interfaces are completely empty interfaces.
  
  Eg: Serializable, Cloneable

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/2f150129-7b35-488d-9c64-f9cbdea809a8)

--------------------------
