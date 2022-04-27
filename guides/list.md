# List

Lists are used to store multiple items in a single variable.

Lists are one of 4 built-in data types in Python used to store collections of data, the other 3 are [Tuple](https://www.w3schools.com/python/python\_tuples.asp), [Set](https://www.w3schools.com/python/python\_sets.asp), and [Dictionary](https://www.w3schools.com/python/python\_dictionaries.asp), all with different qualities and usage.

Lists are created using square brackets:

```
//Create a List:

thislist = ["apple", "banana", "cherry"]
print(thislist)
```

### List Items

List items are ordered, changeable, and allow duplicate values.

List items are indexed, the first item has index `[0]`, the second item has index `[1]` etc.

### Ordered

When we say that lists are ordered, it means that the items have a defined order, and that order will not change.

If you add new items to a list, the new items will be placed at the end of the list.

### Changeable

The list is changeable, meaning that we can change, add, and remove items in a list after it has been created.

***

### Allow Duplicates

Since lists are indexed, lists can have items with the same value:

```
// Example
// Lists allow duplicate values:

thislist = ["apple", "banana", "cherry", "apple", "cherry"]
print(thislist)

```

### List Length

To determine how many items a list has, use the `len()` function:

```
// Example
Print the number of items in the list:

thislist = ["apple", "banana", "cherry"]
print(len(thislist))

```

### List Items - Data Types

List items can be of any data type:

```
// Example
//String, int and boolean data types:

list1 = ["apple", "banana", "cherry"]
list2 = [1, 5, 7, 9, 3]
list3 = [True, False, False]
```

A list can contain different data types:

```
//Example
//A list with strings, integers and boolean values:

list1 = ["abc", 34, True, 40, "male"]
```

### type()

From Python's perspective, lists are defined as objects with the data type 'list':

```
<class 'list'>
```

#### Example

What is the data type of a list?

```
// code
mylist = ["apple", "banana", "cherry"]
print(type(mylist))
```

### The list() Constructor

It is also possible to use the list() constructor when creating a new list.

```
// Example
// Using the list() constructor to make a List:

thislist = list(("apple", "banana", "cherry")) # note the double round-brackets
print(thislist)
```

### Python Collections (Arrays)

There are four collection data types in the Python programming language:

* **List** is a collection which is ordered and changeable. Allows duplicate members.
* [**Tuple**](https://www.w3schools.com/python/python\_tuples.asp) is a collection which is ordered and unchangeable. Allows duplicate members.
* [**Set**](https://www.w3schools.com/python/python\_sets.asp) is a collection which is unordered, unchangeable\*, and unindexed. No duplicate members.
* [**Dictionary**](https://www.w3schools.com/python/python\_dictionaries.asp) is a collection which is ordered\*\* and changeable. No duplicate members.

\*Set _items_ are unchangeable, but you can remove and/or add items whenever you like.

\*\*As of Python version 3.7, dictionaries are _ordered_. In Python 3.6 and earlier, dictionaries are _unordered_.

When choosing a collection type, it is useful to understand the properties of that type. Choosing the right type for a particular data set could mean retention of meaning, and, it could mean an increase in efficiency or security.

### &#x20;Python - Access List Items

### Access Items

List items are indexed and you can access them by referring to the index number:

```
// Example
// Print the second item of the list:

thislist = ["apple", "banana", "cherry"]
print(thislist[1])
```

**Note:** The first item has index 0.

#### Negative Indexing

Negative indexing means start from the end

`-1` refers to the last item, `-2` refers to the second last item etc.

```
// Example
// Print the last item of the list:

thislist = ["apple", "banana", "cherry"]
print(thislist[-1])
```

#### Range of Indexes

You can specify a range of indexes by specifying where to start and where to end the range.

When specifying a range, the return value will be a new list with the specified items.

```
// Example
// Return the third, fourth, and fifth item:

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])
```

**Note:** The search will start at index 2 (included) and end at index 5 (not included).

Remember that the first item has index 0.

By leaving out the start value, the range will start at the first item:

```
// Example
// This example returns the items from the beginning to, but NOT including, "kiwi":

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[:4])
```

By leaving out the end value, the range will go on to the end of the list:

#### Range of Negative Indexes

Specify negative indexes if you want to start the search from the end of the list:

```
// Example
// This example returns the items from "orange" (-4) to, but NOT including "mango" (-1):

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[-4:-1])
```

### Check if Item Exists

To determine if a specified item is present in a list use the `in` keyword:

```
// Example
// Check if "apple" is present in the list:

thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")
```
