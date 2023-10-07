# Datatypes

## Python Data Types

Variables can hold values, and every value has a data-type. Python is a dynamically typed language; hence we do not need to define the type of the variable while declaring it. The interpreter implicitly binds the value with its type.

`a = 5`&#x20;

The variable **a** holds integer value five and we did not define its type. Python interpreter will automatically interpret variables **a** as an integer type.

Python enables us to check the type of the variable used in the program. Python provides us the **type()** function, which returns the type of the variable passed.

Consider the following example to define the values of different data types and checking its type.

```python
// Some code
a=10  
b="Hi Python"  
c = 10.5  
print(type(a))  
print(type(b))  
print(type(c))  
```

Python has the following data types built-in by default, in these categories:

| Text Type:      | `str`                              |
| --------------- | ---------------------------------- |
| Numeric Types:  | `int`, `float`, `complex`          |
| Sequence Types: | `list`, `tuple`, `range`           |
| Mapping Type:   | `dict`                             |
| Set Types:      | `set`, `frozenset`                 |
| Boolean Type:   | `bool`                             |
| Binary Types:   | `bytes`, `bytearray`, `memoryview` |

### Getting the Data Type

You can get the data type of any object by using the `type()` function:

#### Example

Print the data type of the variable x:

```python
x = 5
print(type(x))
```



### Setting the Specific Data Type

If you want to specify the data type, you can use the following constructor functions:

### Setting the Specific Data Type

If you want to specify the data type, you can use the following constructor functions:

<table><thead><tr><th width="491">Example</th><th width="552.3333333333333">Data Type</th><th></th><th>Try it</th></tr></thead><tbody><tr><td>x = str("Hello World")</td><td>str</td><td></td><td></td></tr><tr><td>x = int(20)</td><td>int</td><td></td><td></td></tr><tr><td>x = float(20.5)</td><td>float</td><td></td><td></td></tr><tr><td>x = complex(1j)</td><td>complex</td><td></td><td></td></tr><tr><td>x = list(("apple", "banana", "cherry"))</td><td>list</td><td></td><td></td></tr><tr><td>x = tuple(("apple", "banana", "cherry"))</td><td>tuple</td><td></td><td></td></tr><tr><td>x = range(6)</td><td>range</td><td></td><td></td></tr><tr><td>x = dict(name="John", age=36)</td><td>dict</td><td></td><td></td></tr><tr><td>x = set(("apple", "banana", "cherry"))</td><td>set</td><td></td><td></td></tr><tr><td>x = frozenset(("apple", "banana", "cherry"))</td><td>frozense</td><td></td><td></td></tr><tr><td>x = bool(5)</td><td>bool</td><td></td><td></td></tr><tr><td>x = bytes(5)</td><td>bytes</td><td></td><td></td></tr><tr><td>x = bytearray(5)</td><td>bytearray</td><td></td><td></td></tr><tr><td>x = memoryview(bytes(5))</td><td>memoryview</td><td></td><td></td></tr></tbody></table>
