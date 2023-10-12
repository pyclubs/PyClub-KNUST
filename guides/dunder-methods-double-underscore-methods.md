# Dunder Methods(Double Underscore Methods)

Dunder methods, short for "double underscore" methods but often referred to as "magic methods" or "special methods," are special functions in Python that have double underscores at the beginning and end of their names, like `__init__` or `__str__`. These methods have specific meanings and purposes in Python, and they allow you to define how objects of your custom classes behave in various situations.

&#x20;

Here are some commonly used dunder methods in Python:

&#x20;

1\. `__init__`: This method is used to initialize an object's attributes when it's created.

&#x20; &#x20;

```python
class MyClass:
       def __init__(self, value):
           self.value = value
 
   obj = MyClass(42)
```

2\. ``__str__` and __repr__``: These methods control how an object is represented as a string when using \`str(obj)\` or \`repr(obj)\`, respectively.

&#x20;&#x20;

```python
 class MyClass:
       def __init__(self, value):
           self.value = value
 
       def __str__(self):
           return f"MyClass instance with value: {self.value}"
 
       def __repr__(self):
           return f"MyClass({self.value})"
 
   obj = MyClass(42)
   print(obj)         # Output: MyClass instance with value: 42
   print(repr(obj))   # Output: MyClass(42)
 
```

3.`__eq__`: This method is used to define custom equality comparisons for objects of a class.

&#x20; &#x20;

```python
class Point:
       def __init__(self, x, y):
           self.x = x
           self.y = y
 
       def __eq__(self, other):
           return self.x == other.x and self.y == other.y
 
   p1 = Point(1, 2)
   p2 = Point(1, 2)
   print(p1 == p2)  # Output: True
```

4.`__len__`: This method allows you to define the behavior of \``len(obj)`\` for objects of your class.

&#x20;&#x20;

```python
 class MyList:
       def __init__(self, elements):
           self.elements = elements
 
       def __len__(self):
           return len(self.elements)
 
   my_list = MyList([1, 2, 3])
   print(len(my_list))  # Output: 3
```

5.`_add__`: You can use this method to define custom behavior for the \`+\` operator when applied to objects of your class.

&#x20;

```python
class Vector:
       def __init__(self, x, y):
           self.x = x
           self.y = y
 
       def __add__(self, other):
           return Vector(self.x + other.x, self.y + other.y)
 
   v1 = Vector(1, 2)
   v2 = Vector(3, 4)
   result = v1 + v2
```

These are just a few examples of dunder methods, but Python provides many more. Using dunder methods allows you to customize the behavior of your classes and make them more Pythonic, intuitive, and compatible with built-in functions and operators.

1\. \``__init__(self, ...)`\`: Constructor method, called when an object is created.

&#x20;

2\. \``` __del__(self)` ``: Destructor method, called when an object is about to be destroyed.

&#x20;

3\. \``__str__(self)`\`: Controls the string representation of an object when using \`str(obj)\`.

&#x20;

4\. \``` __repr__(self)` ``: Controls the official string representation of an object when using \`repr(obj)\`.

&#x20;

5\. \``__len__(self)`\`: Defines the behavior of \`len(obj)\` for objects of your class.

&#x20;

6\. \``__getitem__(self, key)`\`: Allows object indexing, e.g., \`obj\[key]\`.

&#x20;

7\. \``__setitem__(self, key, value)`\`: Allows assignment to object elements, e.g., \`obj\[key] = value\`.

&#x20;

8\. \``__delitem__(self, key)`\`: Controls item deletion with \`del obj\[key]\`.

&#x20;

9\. \``` __iter__(self)` ``: Returns an iterator for the object, used in loops.

&#x20;

10\. \``__next__(self)`\`: Defines the behavior when iterating over an object.

&#x20;

11\. \``__contains__(self, item)`\`: Controls the behavior of the \`in\` operator, e.g., \`item in obj\`.

&#x20;

12\. \``__eq__(self, other)`\`: Defines custom equality comparisons using \`==\`.

&#x20;

13\. \``__ne__(self, other)`\`: Defines custom inequality comparisons using \`!=\`.

&#x20;

14\. \`\_`_lt__(self, other)`\`: Defines custom less-than comparisons using \`<\`.

&#x20;

15\. \``` __le__(self, other)` ``: Defines custom less-than-or-equal-to comparisons using \`<=\`.

&#x20;

16\. \``__gt__(self, other)`\`: Defines custom greater-than comparisons using \`>\`.

&#x20;

17\. \``` __ge__(self, other)` ``: Defines custom greater-than-or-equal-to comparisons using \`>=\`.

&#x20;

18\. \``` __add__(self, other)` ``: Defines custom behavior for the \`+\` operator.

&#x20;

19\. \```__sub__(self, other)`:`` Defines custom behavior for the \`-\` operator.

&#x20;

20\. \`\_`` _mul__(self, other)` ``: Defines custom behavior for the \`\*\` operator.

&#x20;

21\. \``` __truediv__(self, other)` ``: Defines custom behavior for the \`/\` operator.

&#x20;

22\. \``` __floordiv__(self, other)` ``: Defines custom behavior for the \`//\` operator.

&#x20;

23\. \``` __mod__(self, other)` ``: Defines custom behavior for the \`%\` operator.

&#x20;

24\. \``` __pow__(self, other[, modulo])` ``: Defines custom behavior for the \`\` operator.

&#x20;

25\. `` `__contains__(self, item)` ``: Controls membership tests using the \`in\` keyword.

&#x20;

26\. `` `__call__(self, ...)` ``: Allows objects to be called as functions.

&#x20;

27\. `` `__enter__(self)`, `__exit__(self, exc_type, exc_value, traceback) ``\`: Used for context management with the \`with\` statement.

&#x20;

These are some of the most commonly used dunder methods in Python. Depending on the context and the specific requirements of your classes, you may choose to implement one or more of these methods to customize their behavior.
