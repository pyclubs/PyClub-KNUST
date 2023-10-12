---
description: >-
  Iterators and generators are powerful features in Python that allow you to
  work with sequences of data efficiently. In this tutorial, we will explore
  iterators and generators, how they work, and when
---

# Iterator and Generator

**Iterators**

An iterator is an object that represents a stream of data. You can iterate (loop) over the elements of an iterator one at a time. Python provides two essential methods for working with iterators: `__iter__()` and `__next__()`.

1. **Creating an Iterator:**

&#x20;To create an iterator, you need to define a class with two methods: `` `__iter__()` `` and `` `__next__()` ``. The `` `__iter__() ``\` method returns the iterator object itself, and the `` `__next__()` `` method returns the next value from the iterator.



```python
class MyIterator:
       def __init__(self):
           self.values = [1, 2, 3, 4, 5]
           self.index = 0
       def __iter__(self):
           return self
       def __next__(self):
           if self.index < len(self.values):
               result = self.values[self.index]
               self.index += 1
               return result
           else:
               raise StopIteration
```

**2. Using an Iterator:**

To use an iterator, you can create an instance of the iterator class and use a `` `for` `` loop to iterate over its elements.

&#x20;&#x20;

```python
 my_iterator = MyIterator()
  for value in my_iterator:
       print(value)
```

&#x20;  This will print the numbers 1 through 5.

&#x20;

**Generators**

Generators provide a more concise and convenient way to create iterators. They are defined as functions using the \`yield\` keyword. When a function contains one or more \`yield\` statements, it becomes a generator. Generator functions do not execute immediately; they return a generator object that can be iterated over.

**1. Creating a Generator:**

&#x20;Here's how you can define a generator function:

&#x20;

```python
def my_generator():
       yield 1
       yield 2
       yield 3
       yield 4
       yield 5
```

&#x20;

**2. Using a Generator:**

To use a generator, you can call the generator function, which returns a generator object. You can then iterate over the values it yields using a \`for\` loop.

&#x20;&#x20;

```python
gen = my_generator()
   for value in gen:
       print(value)
```

This will also print the numbers 1 through 5.

&#x20;**Generator Expressions**

Generator expressions provide a concise way to create generators. They are similar to list comprehensions but use parentheses instead of square brackets.



```python
gen_expr = (x for x in range(1, 6))
for value in gen_expr:
   print(value)
```

This code will produce the same result as the previous examples.



&#x20; **When to Use Iterators and Generators**

* Use iterators when you need to create a custom iterable object with more complex logic.
* Use generators when you want a simpler way to create iterable sequences, especially for large data sets, as they are memory-efficient.
* Generator expressions are handy for creating simple generators on the fly.
