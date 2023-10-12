# Decorators

Python decorators are a powerful and versatile feature used for modifying or enhancing the behavior of functions or methods without changing their source code. They are often used for tasks like logging, authentication, and memoization. Here's an explanation of decorators with examples:

**1. Basics of Decorators:**

In Python, decorators are functions that take another function as an argument and return a new function that usually extends or modifies the behavior of the input function. Decorators are commonly denoted using the "@" symbol in Python

**2. Creating a Simple Decorator:**

&#x20;

Here's a simple decorator that logs the execution of a function:

def log\_function\_execution(func):

&#x20;&#x20;

```python
 def wrapper(*args, kwargs):
        print(f"Calling function: {func.__name__}")
        result = func(*args, kwargs)
        print(f"{func.__name__} executed")
        return result
    return wrapper
 
@log_function_execution
def say_hello():
    print("Hello!")
 
say_hello()
```

When you call \`say\_hello\`, it gets wrapped by the \`log\_function\_execution\` decorator, and additional logging is performed before and after the \`say\_hello\` function is executed.

&#x20;

**3. Decorating Functions with Arguments:**

&#x20;

You can also create decorators that accept arguments. Here's an example:

```python
def repeat_n_times(n):
    def decorator(func):
        def wrapper(*args, kwargs):
            for _ in range(n):
                result = func(*args, kwargs)
            return result
        return wrapper
    return decorator
 
@repeat_n_times(n=3)
def say_hi():
    print("Hi!")
 
say_hi()
```

&#x20;

In this example, the \`repeat\_n\_times\` decorator takes an argument \`n\`, and you can apply it to functions with different repeat counts.

&#x20;

**4. Class-Based Decorators:**



Decorators can also be implemented as classes. Here's an example:

```python
class TimerDecorator:
    def __init__(self, func):
        self.func = func
   
    def __call__(self, *args, kwargs):
        import time
        start_time = time.time()
        result = self.func(*args, kwargs)
        end_time = time.time()
        print(f"{self.func.__name__} took {end_time - start_time} seconds")
        return result
 
@TimerDecorator
def slow_function():
    import time
    time.sleep(2)
 
slow_function()
```

In this example, the `` `TimerDecorator` `` class is used as a decorator to measure the execution time of the `` `slow_function` ``.

**5. Built-in Decorators:**

Python also has several built-in decorators like `` `@staticmethod ``\`, `` `@classmethod ``\`, and `` `@property ``\`. These decorators provide special behavior to methods in classes.

Decorators are a powerful tool for enhancing the functionality and behavior of Python functions and methods while keeping the code clean and maintainable. Understanding decorators is crucial for more advanced Python programming and building clean and reusable code.

&#x20;
