
# Collection Hierarchy

## Top level - Only Interfaces
```bash
                                              java.lang.Iterable (Interface)  
                            Java 8: 1. default void forEach(Consumer<? super T> action)
                                    2. default Spliterator<T> spliterator()               
                                                         |  
                                                         |  
                                             java.util.Collecton (Interface)  
                            Java 8: 1. default boolean removeIf(Predicate<? super E> filter)
                                    2. default Stream<E> stream()
                                    3. default Stream<E> parallelStream() 
                                                         |  
                  _______________________________________|_____________________________________  
                 |                                       |                                     |  
                 |                                       |                                     |  
    java.util.List (Interface)                           |                              java.util.Queue  
1. default void replaceAll(UnaryOperator<E> operator)    |                                (Interface)
2. default void sort(Comparator<? super E> c)            |                                      |
3. default Spliterator<E> spliterator() (overridden)     |                              java.util.Deque
                                                         |                                (Interface)
                                                    java.util.Set (Interface)    
                                       1. default Spliterator<E> spliterator() (overridden)
                      
                      
 ```

## Abstraction - Abstract classes for less work in concrete implementations

```bash

                                             java.util.Collecton (Interface)
                                                         |  
                                                         |
                                           AbstractCollection (Abstract class)
                                                         |
                  _______________________________________|_____________________________________ 
                 |                                       |                                     |
                 |                                       |                                     |  
           AbstractList                               AbstractSet                       AbstractQueue 
         (abstract class)                           (abstract class)                 (abstract class)
                 |
                 |
      AbstractSequentialList
         (abstract class)

```
```java
public abstract class AbstractCollection<E> implements Collection<E> {} 
public abstract class AbstractList<E> extends AbstractCollection<E> implements List<E> {}
public abstract class AbstractSequentialList<E> extends AbstractList<E> {}
public abstract class AbstractSet<E> extends AbstractCollection<E> implements Set<E> {}
public abstract class AbstractQueue<E> extends AbstractCollection<E> implements Queue<E> {}
```

## List - Ordered, Duplicates
 
```bash
                                            
                                            java.util.List (Interface)
                                                   |  
                  _________________________________|________________________________  
                 |                                 |                                 |  
                 |                                 |                                 |
          ArrayList (Class)                Vector(Class)                     LinkedList (Class)
(use when frequent access to data is required)                  (use when multiple add remove is required)

Note: It is good practise to initialize ArrayList with higher initial capacity as default is less (10)
```
```java
public class ArrayList<E> extends AbstractList<E> implements List<E>, RandomAccess, Cloneable, Serializable
public class Vector<E> extends AbstractList<E> implements List<E>, RandomAccess, Cloneable, java.io.Serializable
public class LinkedList<E> extends AbstractSequentialList<E> implements List<E>, Deque<E>, Cloneable,Serializable

// Common Marker Interfaces:
java.lang.Cloneable: for cloning 
java.io.Serialiazable: Serializability of a class is enabled by implementing
java.util.RandomAccess: indicate that they support fast (generally constant time) random access
```


## Set - No Duplicates
 
```bash
                                            
                                            java.util.Set (Interface)
                                                   |  
                  _________________________________|________________________________  
                 |                                                                  |  
                 |                                                                  |
  java.util.SortedSet (Interface)                           {unordered} java.util.HashSet (Class)
               |                                                                    |                       
               |                                                                    |
  java.util.NavigableSet (Interface)                     {ordered} java.util.LinkedHashSet (Class)      
               |                           (It also implements Set but its useless, see reference)
               |
  java.util.TreeSet (Class) {Sorted, hence elements must implement java.lang.Comparable}          
(considers only compare/compareTo for equality and duplicacy as well, NO Equals and Hashcode here)
```
```java
public class HashSet<E> extends AbstractSet<E> implements Set<E>, Cloneable, java.io.Serializable{}
public class LinkedHashSet<E> extends HashSet<E> implements Set<E>, Cloneable, java.io.Serializable{}
public class TreeSet<E> extends AbstractSet<E> implements NavigableSet<E>, Cloneable, java.io.Serializable
```

**Reference why LinkedhashSet implements Set when already extending HashSet:**  
https://stackoverflow.com/questions/2165204/why-does-linkedhashsete-extend-hashsete-and-implement-sete  


## Queue - Ordered
 
```bash
                                            
                                            java.util.Queue (Interface)
                                                   |  
                  _________________________________|________________________________ 
                 |                                 |                                |
                 |                                 |                                |
          java.util.Deque        java.util.concurrent.BlockingQueue        java.util.PriorityQueue
             (Interface)                      (Interface)                        (Class)
                 |                                 | 
       __________|____________                     |
      |                       |             BlockingDequeue
      |                       |       (Concurrent package Interface)
ArrayDeque               LinkedList
(Class)                   (Class)
```
```java
public class ArrayDeque<E> extends AbstractCollection<E> implements Deque<E>, Cloneable, Serializable
public class LinkedBlockingDeque<E> extends AbstractQueue<E> implements BlockingDeque<E>, Serializable
public class LinkedBlockingQueue<E> extends AbstractQueue<E> implements BlockingQueue<E>, Serializable
public class PriorityQueue<E> extends AbstractQueue<E> implements java.io.Serializable
```

## Map - key value data

```bash
                                            java.util.Map (Interface)
                                                   |  
                  _________________________________|________________________________  
                 |                                 |                                |  
                 |                                 |                                |
  java.util.SortedMap (Interface)              Hashtable       {unordered} java.util.HashMap (Class)
                 |                                                                  |             
                 |                                                                  |
  java.util.NavigableMap (Interface)                     {ordered} java.util.LinkedHashMap (Class) 
                 |
                 |
  java.util.TreeMap (Class) {Sorted, hence keys must implement java.lang.Comparable} 
```
```java  
public class Hashtable<K,V> extends Dictionary<K,V> implements Map<K,V>, Cloneable, Serializable
public class HashMap<K,V> extends AbstractMap<K,V> implements Map<K,V>, Cloneable, Serializable
public class LinkedHashMap<K,V> extends HashMap<K,V> implements Map<K,V>
public class TreeMap<K,V> extends AbstractMap<K,V> implements NavigableMap<K,V>, Cloneable, Serializable
```

## Streams - Bulk data operation

```bash

                                         java.util.stream.BaseStream (Interface)
                                                   |  
        ___________________________________________|_______________________________________  
        |                             |                           |                       |
        |                             |                           |                       |
Stream(Interface)            IntStream(Interface)     LongStream(Interface)    DoubleStream(Interface)
```
```java
public interface BaseStream<T, S extends BaseStream<T, S>> extends AutoCloseable {}
public interface Stream<T> extends BaseStream<T, Stream<T>> {}
public interface IntStream extends BaseStream<Integer, IntStream> {}
public interface LongStream extends BaseStream<Long, LongStream> {}
public interface DoubleStream extends BaseStream<Double, DoubleStream> {}
```

# Exception Hierarchy

```bash
                                        java.lang.Throwable (Class)
                                         (Checked/Compile time)
                                                   |  
                      _____________________________|______________________________  
                     |                                                            |  
                     |                                                            |
            java.lang.Exception (Class)                                java.lang.Error (Class)
              (Checked/Compile time)                                    (un-checked/run time)
                     |
         ____________|_____________
        |                          |
        |                          |
 Runtime Exception         Other Exceptions
(un-checked/run time)    (Checked/Compile time)

```

# Lock Hierarchy

```bash
                                        java.util.concurrent.locks.Lock(Interface) 
                                                         |
                  _______________________________________|_________________________________ 
                 |                                       |                                 |
                 |                                       |                                 |
       Read Lock(static class)                 WriteLock (static class)          ReentrantLock(class)
```
```java
public class ReentrantLock implements Lock, java.io.Serializable {}

public class ReentrantReadWriteLock implements ReadWriteLock, java.io.Serializable {
  * public static class ReadLock implements Lock, java.io.Serializable {}
  * public static class WriteLock implements Lock, java.io.Serializable {}
}
public class StampedLock implements java.io.Serializable {(Java 8)
  * final class WriteLockView implements Lock {}
  * final class ReadLockView implements Lock {}
}
```

# Executor Framework

```bash
   
                                       java.util.concurrent.Executor (Interface)
                                                         |  
                                                         |
                                    java.util.concurrent.ExecutorService (Interface)
                                                         |
                        _________________________________|_________________________________ 
                       |                                                                   |
                       |                                                                   |  
        AbstractExecutorService(abstract class)                         ScheduledExecutorService(Interface)
                       |
         ______________|_______________
        |                              |
        |                              |
ThreadPoolExecutor                ForkJoinPool
   (Class)                     (Class, since 1.7) 
        |
        |
ScheduledThreadPoolExecutor
(also implements ScheduledExecutorService)
```        
```java        
public interface ExecutorService extends Executor {}
public abstract class AbstractExecutorService implements ExecutorService {} 
public interface ScheduledExecutorService extends ExecutorService {}
public class ThreadPoolExecutor extends AbstractExecutorService {}
public class ForkJoinPool extends AbstractExecutorService {}
public class ScheduledThreadPoolExecutor extends ThreadPoolExecutor implements ScheduledExecutorService{} 

Factory class to get above implementations:
public class java.util.concurrent.Executors
```
