---
description: What is an Array?
---

# Arrays

An array is a special variable, which can hold more than one value at a time.

If you have a list of items (a list of car names, for example), storing the cars in single variables could look like this.

```python
car1 = "Ford"
car2 = "Volvo"
car3 = "BMW"
```

However, what if you want to loop through the cars and find a specific one? And what if you had not 3 cars, but 300?

The solution is an array!

An array can hold many values under a single name, and you can access the values by referring to an index number.

### Access the Elements of an Array

You refer to an array element by referring to the _index number_.

Get the value of the first array item:

x = cars\[0]

#### Example

```python
// Get the value of the first array item:

x = cars[0]
```

```
// Modify the value of the first array item:

cars[0] = "Toyota"
```

{% hint style="info" %}
**Note:** The length of an array is always one more than the highest array index.
{% endhint %}

### Looping Array Elements

You can use the `for in` loop to loop through all the elements of an array.

#### Example

```python
// Print each item in the cars array:
for x in cars:
  print(x)
```

### Adding Array Elements

You can use the `append()` method to add an element to an array.

#### Example

```python
// Add one more element to the cars array:
cars.append("Honda")
```

```
Removing Array Elements
You can use the pop() method to remove an element from the array.
```

```python
// Delete the second element of the cars array:

cars.pop(1)
```

You can also use the `remove()` method to remove an element from the array.

#### Example

```python
// Delete the element that has the value "Volvo":
cars.remove("Volvo")
```

{% hint style="info" %}
The list's `remove()` method only removes the first occurrence of the specified value.
{% endhint %}

Array Methods

Python has a set of built-in methods that you can use on lists/arrays.

| Method                                                               | Description                                                                  |
| -------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [append()](https://www.w3schools.com/python/ref\_list\_append.asp)   | Adds an element at the end of the list                                       |
| [clear()](https://www.w3schools.com/python/ref\_list\_clear.asp)     | Removes all the elements from the list                                       |
| [copy()](https://www.w3schools.com/python/ref\_list\_copy.asp)       | Returns a copy of the list                                                   |
| [count()](https://www.w3schools.com/python/ref\_list\_count.asp)     | Returns the number of elements with the specified value                      |
| [extend()](https://www.w3schools.com/python/ref\_list\_extend.asp)   | Add the elements of a list (or any iterable), to the end of the current list |
| [index()](https://www.w3schools.com/python/ref\_list\_index.asp)     | Returns the index of the first element with the specified value              |
| [insert()](https://www.w3schools.com/python/ref\_list\_insert.asp)   | Adds an element at the specified position                                    |
| [pop()](https://www.w3schools.com/python/ref\_list\_pop.asp)         | Removes the element at the specified position                                |
| [remove()](https://www.w3schools.com/python/ref\_list\_remove.asp)   | Removes the first item with the specified value                              |
| [reverse()](https://www.w3schools.com/python/ref\_list\_reverse.asp) | Reverses the order of the list                                               |
| [sort()](https://www.w3schools.com/python/ref\_list\_sort.asp)       | Sorts the list                                                               |

