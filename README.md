# 19CS301-Module10
###EX: 10.a  STACK
### Aim: To Write a python programming to sort the stack using recursion
### Algorithm:
STEP 1: Start.

STEP 2: Define sortStack(stack) to sort recursively by popping all elements.

STEP 3: Recursively call sortStack until the stack is empty.

STEP 4: Use sortedInsert(stack, key) to insert each popped element back in sorted order.

STEP 5: In sortedInsert, if the stack is empty or key > top, push key.

STEP 6 : Else, pop top, recursively insert key, then push top back.

STEP 7: Read input, call sortStack, and print the result.

STEP 8: Stop.

### Program:
```
def sortedInsert(stack, key):
    if not stack or key > stack[-1]:
        stack.append(key)
        return
    top = stack.pop()
    sortedInsert(stack, key)
    stack.append(top)
def sortStack(stack):
    if not stack:
        return
 
    top = stack.pop()
    sortStack(stack)
    sortedInsert(stack, top)

 
A = eval(input())
sortStack(A)
print(list(A))
```
### Output:
 ![image](https://github.com/gokulkrishnan2005/19CS301-Module10/blob/main/module10-1.png)

### Result: Thus, the given program is implemented and executed successfully .
 


### EX: 10.2 IMPLEMENTATION OF STACK
### Aim: To Write a  python program to add only the even unique numbers using appendleft() from n given numbers.
### Algorithm:

STEP 1: Start.

STEP 2: Import collections and import deque.

STEP 3: Create an empty queue using deque.

STEP 4: Read n numbers from input.

STEP 5 : For each number, check if it is even and not already in the queue.

STEP 6: If valid, insert it at the front using appendleft().

STEP 7 : Print the result. 

STEP 8 : Stop.
### Program: 
```
from collections import deque
class Queue:  
  def __init__(self):  
      self.queue = deque()  
  def add_element(self,val):
      if val%2==0 and val not in self.queue:  
          self.queue.appendleft(val)  
          return True  
      return False  
TheQueue = Queue()  
n=int(input())
for i in range(n):
    TheQueue.add_element(int(input())) 
print(TheQueue.queue)
```
### Output:
![image](https://github.com/user-attachments/assets/f42c4ec6-578c-418a-8f66-cf70abe7dc54)

### Result: Thus, the given program is implemented and executed successfully .
 


EX: 10.3 QUEUE
### Aim: To Write a python program to implement the stack using deque method for rotating the stack.
### Algorithm:

STEP 1: Start.

STEP 2: Import collections and import deque.

STEP 3: Create a stack and a variable n.

STEP 4: Get the number of inputs from user.

STEP 5: Using a loop get the inputs from user.

STEP 6: Append the even and unique elements in the stack.

STEP 7: Print the result.
### Program:
```
import collections
stack = collections.deque([])
n = int(input())
for i in range(n):
       x = int(input())
        if x not in stack:
          if x%2==0:
             stack.appendleft(x)
print(stack)
```
### Output:
![image](https://github.com/user-attachments/assets/de6e3e09-b10b-42d4-9faf-32fcf990f29a)
 
### Result: Thus, the given program is implemented and executed successfully .


### EX: 10.4 IMPLEMENTATION OF QUEUE
### Aim: To Develop a python program to get the 4 integer values from user and display the values using multiprocessing library
### Algorithm:

STEP 1: Start.

STEP 2: From Multiprocessing Import Queue.

STEP 3: Create a list and get the input from user.

STEP 4 : Append the elements in the list.

STEP 5: Using 'get' built-in function print the list.

STEP 6 : Print the result.

STEP 7 : Stop.
### Program:
```
from multiprocessing import Queue
queue = Queue()
for i in range(4):
    queue.put(int(input()))
for i in range(4):
     print(queue.get())
```
### Output:
 ![image](https://github.com/user-attachments/assets/26a380ff-118e-43f4-8178-83a5417262b5)
 

### Result: Thus, the given program is implemented and executed successfully .
 

