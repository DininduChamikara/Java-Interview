# Java Interview 
This repository is designed to help you to face Java interviews with confidence.

## Important Points 

* In object-oriented programming, a synchronized method is a method that can only be accessed by one thread at a time, while a non-synchronized method can be accessed by multiple threads simultaneously.
* Exception is an event which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.”

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

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/a7422ffa-f526-4a2e-9854-e5e6fe41e9bf)


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

## Top Tricky Interview Questions on Collection Framework
video - https://www.youtube.com/watch?v=KfoNYoVUBJI&list=PLyHJZXNdCXscoyL5XEZoHHZ86_6h3GWE1&index=2

1. Explain Collection Hierarchy

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/02c358f6-d684-42f9-8140-5f4cc706f2dc)


* java.util.Collection is the root of the Java Collection framework and most of the collections in Java are inherited from this interface except Map Interface.
* The 3 basic interfaces which implement / extend the collection framework:
  * List
  * Queue
  * Set

* List
  - Contains ordered elements.
  - May include duplicates.
  - Supports the index-based search, random access but elements can be easily inserted irrespective of the position.
 
* Set
  - Doesn't define an order for the elements hence index based search is not supported.
  - Doesn't contain duplicates. 

* Queue
  - follows a FIFO approach

* Map
  - Represent Key, Value pair
  - Map interface does not implement the Collection.
  - It can only contain a unique key.
  - Can have duplicate values.

### List Interface

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/614977ef-0317-4a48-8e0e-fa8076c88427)

* ArrayList
  - Dynamic resizing -> 50% from original size
  - Non synchronized

* Linked list
  - implements List and Deque interfaces.
  - maintains the insertion order.
  - Non syncronized.
  - does not support accessing elements randomly. Only iterate through the linked list.

* Vector
  - Vector is synchronized.
  - maintains the insertion order.
  - It's Thread safe.
  - Vactor increases its size by doubling the array size.

* Stack
  - follows the LIFO approach


### Set Interface

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/1962083c-ba9d-4d8b-9dab-908822d2b959)

* Hash Set
  - It implicitly implements a hashtable.
  - Contains only unique elements.
  - only one null element can be added.
  - It is unordered as set.

* Linked HashSet
   - ordered version of HashSet which maintains a doubly-linked List across all elements.
   - It preserves the insertion order. 

* Sorted Set
  - All elements of a SortedSet must implement the Comparable interface.
  - It's a set sorted in an ascending order.
 
* Tree Set
  - Uses a Tree for storage
  - Objects in a TreeSet are stored in a sorted and ascending order.


### Queue Interface

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/3c1abc3a-df30-4a4d-81fa-49e819042d71)

* Priority Queue
  - Priority Queue is a queue with priority associated with each element.
  - A high-priority element is served before a low-priority element irrespective of their insertion order. 

* Deque
  - Deque Refers to a double-ended queue.
  - Elements can be added and removed from either end. 

* ArrayDeQue
  - Way to apply resizable array in addition to the implementation of the Deque interface.
  - no capacity restrictions.
 

### Map Interface

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/e92acc61-70f2-479f-93e6-a337c6173345)

* Hash Map
  - It is non-synchronized in nature.
  - Allows only one null key but multiple null values.

* Hash Table
  - It is synchronized in nature.
  - Doesn't allow any null key or value.

* Sorted Map
  - entries are maintained in an ascending key order.
------------------------- 

2. Why Map doesn't extend the Collection Interface?

* The Map Interface in Java follows a key/value pair structure.
* Collection interface is a collection of objects that are stored in a structured manner with a specified access mechanism.
* The main reason Map doesn't extend the Collection interface is that the add(E e) method of the Collection interface doesn't support the key-value pair like the Map interface's put(K, V) method.

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/99a7bbd5-4f75-4160-baf9-035e8313bc73)


---------------------------

3. Difference between fail-fast and fail-safe iterators

* Fail-fast Iterators throws ConcurrentModificationException when one Thread is iterating over collection object and other thread structurally modify Collection either by adding, removing or modifying objects on underlying collection. They are called fail-fast because they try to immediately throw Exception when they encounter failure.

* Fail-safe iterator doesn't throw any Exception if Collection is modified structurally while one thread is Iterating over it because they work on a clone of Collection instead of the original collection and that's why they are called as fail-safe iterator. 

---------------------------

4. What do you understand by BlockingQueue?

* The Java BlockingQueue interface, java.util.concurrent.BlockingQueue, represent a queue which is thread safe to put elements into, and take elements out of from. In other words, multiple threads can be inserting and taking elements concurrently from a Java Blockingueue, without any concurrency issues arising.

* It is capable of blocking the threads that try to insert or take elements from the queue. For instance, if a thread tries to take an element and there are none left in the queue, the thread can be blocked until there is an element to take. 
--------------------------

5. Difference between Synchronized Collection and Concurrent Collection?

* Both provide thread-safety.
* The differences between them come in performance, scalability and how they achieve thread-safety.
* Syncronized collections like syncronized HashMap are much slower than their concurrent counterparts.
 e.g. ConcurrentHashMap
 - Main reason for this slowness is locking.

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/8bf22d44-aaa3-4ee3-a9ef-e13222e0bec2)

---------------------------

6. Internal working of hash map

* HashMap in Java works on hashing principle where hash functions are used to link key and value in Hashmap, Objects are stored by calling put(key, value) method of HashMap and retrieved by calling get(key) method.

* When we call put method, hashcode() method of the key object is called which calculates an index of the bucket location where we can store the value object.

* To retrieve, you call the get() method and again pass the key object, which lands you up at the same index or bucket and you retrieve the value object.


* If two different keys return the same hash index then collision occurs. In this case, a linked list is formed at that bucket location and a new entry is stored as next node.

* Now put method will just append the object nodes in the linked list.

* But in the case of get if we have a linked list at that index then we need an extra check to search correct value, this is done by equals() method. It checks every key of every node and if equals() returns true, then Map return that corresponding value from the linked list. 

---------------------------

## SQL Interview Questions
video - https://www.youtube.com/watch?v=FJdryrcDD2s

1. How to find the third height Salary?

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/d7f77e4d-e5ca-403d-b20e-070e4b11167d)

* The Below solution is good for the first numbers of the highest salaries.

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/350f4cea-8587-4755-ac4e-252eee2cdfe1)


* For third highest salary,

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/699d8bd7-75b1-4309-a1c0-572a1ba682ba)

LIMIT 2, 1

* 2 = Starting Index
* 1 = number of rows
----------------------------

2. What are Indexes and How to create an index in SQL?

* Indexes are database objects which help in retrieving records quickly and more efficiently.

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/c584fdec-4e05-457f-9d18-608902ef23c2)

![image](https://github.com/DininduChamikara/Java-Interview/assets/73112985/efc7e7ba-856a-497d-a858-19f0f5e9fe9b)

--------------------------

3. How does the index work?

Suppose we need to search by employee name = Manoj

* Behind the scene every single row is checked to see if the employee_name matches with Manoj. (full table scan)
* An index is a data structure that stores the values for a certain specific column of a table and helps avoid a full table scan.
* Database indexing in reality, allows us to cut down the number of rows that need to be examined when a select query with a where clause is executed.

* In SQL,
     - When you create an index, SQL creates a binary tree in a sorted way.
     - then stored that data.
     - 
--------------------------

4. Disadvantages of indexes?

* Indexes take additional space.
* Every time you perform an add, delete, or update operation, the same operation will need to be performed on the index as well.
--------------------------

5. If we drop a table, does it also drop related objects like constraints, indexes, columns, default, views, and stored procedures?

* Yes, the SQL server drops all related objects, that exist inside a table like constraints, indexes, columns, defaults, etc.
* But dropping a table will not drop views and sorted procedures as they exist outside the table. 

---------------------------
