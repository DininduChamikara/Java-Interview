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

* These interfaces tell your compiler then do you have to do something to specific with it.
* It is metadata to your compiler.
* It provides a way to convey information to the compiler or runtime about the intended behavior of a class.
--------------------------

6. Can you override a private or static method in Java?

* You cannot override a private or static method in Java.
* you cannot override a private method in sub class because it's not accessible there, what you do is create another private method with the same name in the child class. Not even visible in the child class.
* For static methods if you create a similar method with same return type and same method arguments in child class then it will hide the superclass method, this is known as method hiding.

* You should always call the static method with the class name.
* With the object reference you can call static methods. You will not get any error. But you should not. 
--------------------------

7. Does "finally" always execute in Java?

Not in the following cases:
* "System.exit()" function
* system crash
--------------------------

8. What methods does the Object Class have?

* Java.lang.Object class, parent of all has following methods:
  * protected Object clone() throws CloneNotSupportedException
       - Creates and returns a copy of this object.
         
  * public boolean equals (Object obj)
       - Indicates whether some other object is "equal to" this one.
         
  * protected void finalize() throws Throwable
       - Called by the garbage collector on an object when garbagecollection determines that there are no more references to the object.

  * public final Class getClass(): Returns the runtime class of an object.
  * public int hashCode(): Returns a hash code value for the object.
  * public String toString(): Returns a string representation of the object.
 
  * public final void notify()
  * public final void notifyAll()
  * public final void wait()
  * public final void wait(long timeout)
  * public final void wait(long timeout, int nanos)
---------------------------

9. How can you make a class immutable?

Six Steps:

* Declare the class as final - so it can't be extended.
* Make all fields private so that direct access is not allowed.
* Don't provide setter methods for variables.
* Make all mutable fields final - so that it's value can be assigned only once.
* Initialize all the fields via a constructor performing a deep copy.
* Perform cloning of objects in the getter methods to return a copy rather than returning the actual object reference.
---------------------------

10. What is singleton class in Java and how can we make a class singleton?

* Singleton class is a class whose only one instance can be created at any given time, in one JVM. 

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/56a81a37-a25e-4120-8060-36e1c00353d7)

* Make your constructor private - no body can create object of it.
* But now you need one object. So, to create one single object you have to create a private static instance of that class itself. 

---------------------------
