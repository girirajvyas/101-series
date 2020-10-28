# Topics
## Time and Space Complexity
 Both these complexities are represented in "Big O notation"   
 Below are the few representations and there quick description  
 
  |  Big O     | Description           |
  | -------    | -----------           |
  | O(1)       | Constant              |
  | O(Log n)   | Logarithmic           |
  | O(n)       | Linear                |
  | O(n x Log n) | Linear x Logarithmic  |
  | O(n^2)     | Polynomial            |
  | O(2^n)     | Exponential           |
  | O(n!)      | Factorial             |
   
  **Tip for Logarithmic Complexities:**  
   Log 1 = 0, Log 10 = 1, Log 100 = 2, Log 1000 = 3, Log 10000 = 4, Log 100000 = 5   
   As we can see value of log is the number of zeroes it has.  
   Hence, **Log of any value between Ten Thousand and 1 Lakh will lie between 4 and 5**   
   e.g.: Log(50,000) = 4.698970004  
   Above comparison will help you in deciding the correct value for algorithms having Logarithmic complexity  
   
  **Performance comparison (for very large values of n i.e n -> infinity ):  
   O(1) < O(Log n) < O(n) < O(n*Log n) < O(n^2) < O(2^n) < O(n!)**
   
   Ref: O(n) vs O(n*Log n)  
   https://stackoverflow.com/questions/21489701/on-log-n-vs-on-practical-differences-in-time-complexity

## Time vs Space Complexity
 
 Example 1:
 ```java
  for (int i=0; i < n; i++) {
    System.out.println("Giri");
  }
 ```
 Time Complexity: O(n)  
 Space Complexity: O(1)    
 
 Example 2:  
 ```java
 List<Integer> newList = new ArrayList<>();
 for (int i=0; i < n; i++) {
   newList.add(i);
 }
 ```
 Time Complexity: O(n)  
 Space Complexity: O(n)   
Ref: https://stackoverflow.com/questions/18686121/differences-between-time-complexity-and-space-complexity/18686162 

## Search Algorithms
  * Linear/Sequential Search
  * Binary Search
     * via divide and conquer
     * via recursion



## Sorting Algorithms 
  * Quick Sort
  * Merge Sort
  * Bubble sort
  
## Performance Summary


|  Algorithm       | Best Time Complexity | Worst Time Complexity | Space Complexity |
| ---------------- | -------------------- | --------------------- | ---------------- |
|  Linear Search   |                      |                       |                  |
|  Binary Search   |         O(1)         |       O(Log n)        |      O(1)        |
|  Quick Sort      |                      |                       |                  |
|  Merger Sort     |                      |                       |                  |
|  Bubble Sort     |                      |                       |                  |
|  Selection Sort  |                      |                       |                  |
|  Insertion Sort  |                      |                       |                  |


## Shift Operators
Ref: https://www.quora.com/Why-is-there-no-unsigned-left-shift-operator-in-Java
