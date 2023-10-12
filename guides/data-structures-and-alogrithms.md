# Data Structures and Alogrithms

Data structures and algorithms are fundamental concepts in computer science and programming. Python provides a rich set of data structures and supports a wide range of algorithms for various tasks.

&#x20;

**Data Structures**

&#x20;**Lists**

A list is a versatile data structure in Python used to store a collection of items. It can hold elements of different data types and is mutable, meaning you can change its contents.

**Creating a List:**

`my_list = [1, 2, 3, 'apple', 'banana', 'cherry']`

&#x20;

**Accessing List Elements:**

`first_item = my_list[0]`

`last_item = my_list[-1]`

&#x20;

**Adding and Removing Elements:**

`my_list.append(4)`                      # Add an element at the end

`my_list.insert(1, 'pear')`       # Insert an element at a specific index

`my_list.remove(2)`                         # Remove the first occurrence of an element

&#x20;

&#x20;`Tuples`

A tuple is similar to a list but is immutable, meaning you cannot change its elements once defined.

**Creating a Tuple:**

**my\_tuple = (1, 2, 3, 'apple', 'banana')**

&#x20;

**Accessing Tuple Elements:**

`first_item = my_tuple[0]`

`last_item = my_tuple[-1]`

&#x20;

&#x20;**Sets**

A set is an unordered collection of unique elements.

**Creating a Set:**

`my_set = {1, 2, 3, 'apple', 'banana'}`

&#x20;

**Adding and Removing Elements:**

`my_set.add(4)`      # Add an element to the set

`my_set.remove(2)`   # Remove an element from the set

&#x20;

&#x20;**Dictionaries**

A dictionary is a key-value pair data structure in Python. It is unordered and mutable.

**Creating a Dictionary:**

`my_dict = {'name': 'John', 'age': 30, 'city': 'New York'}`

&#x20;

**Accessing Dictionary Values:**

`name = my_dict['name']`

`age = my_dict.get('age')`

&#x20;

**Modifying Dictionary:**

`my_dict['city'] = 'San Francisco'`  # Update the value of a key

`my_dict['country'] = 'USA'`                # Add a new key-value pair



### Algorithms

&#x20;**Searching Algorithms**

**1. Linear Search:**

&#x20;  Linear search checks each element in a list sequentially until a match is found.

&#x20;&#x20;

```python
 def linear_search(arr, target):
       for i, item in enumerate(arr):
           if item == target:
               return i
       return -1  # Element not found
```

**2. Binary Search:**

&#x20; Binary search works on sorted lists by repeatedly dividing the search interval in half.

&#x20; &#x20;

```python
def binary_search(arr, target):
       low, high = 0, len(arr) - 1
       while low <= high:
           mid = (low + high) // 2
           if arr[mid] == target:
               return mid
           elif arr[mid] < target:
               low = mid + 1
           else:
               high = mid - 1
       return -1  # Element not found
```

&#x20;

**Sorting Algorithms**

**1. Bubble Sort:**

Bubble sort repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.

&#x20;

```python
def bubble_sort(arr):
       n = len(arr)
       for i in range(n - 1):
           for j in range(0, n - i - 1):
               if arr[j] > arr[j + 1]:
                   arr[j], arr[j + 1] = arr[j + 1], arr[j]
```

&#x20;

**2. Quick Sort:**

Quick sort is a divide-and-conquer algorithm that works by selecting a "pivot" element and partitioning the other elements into two sub-arrays.

```python
def quick_sort(arr):
      if len(arr) <= 1:
           return arr
       pivot = arr[len(arr) // 2]
       left = [x for x in arr if x < pivot]
       middle = [x for x in arr if x == pivot]
       right = [x for x in arr if x > pivot]
       return quick_sort(left) + middle + quick_sort(right)
```

&#x20;**Data Structures and Algorithms Library**

In addition to the above, Python has a built-in library called the Python Standard Library, which includes many useful data structures and algorithms for various tasks. Examples include the \`collections\` module for advanced data structures like \`deque\` and \`Counter\`, and the \`heapq\` module for implementing heaps.
