# Scope

## Python Scope

A variable is only available from inside the region it is created. This is called **scope**.

\
Local Scope

A variable created inside a function belongs to the _local scope_ of that function, and can only be used inside that function

#### Example

A variable created inside a function is available inside that function:

```python
def myfunc():
  x = 300
  print(x)

myfunc()
```

#### Function Inside Function

As explained in the example above, the variable `x` is not available outside the function, but it is available for any function inside the function:

#### Example

The local variable can be accessed from a function within the function:

```python
def myfunc():
  x = 300
  def myinnerfunc():
    print(x)
  myinnerfunc()

myfunc()
```

### Global Scope

A variable created in the main body of the Python code is a global variable and belongs to the global scope.

Global variables are available from within any scope, global and local.

#### Example

A variable created outside of a function is global and can be used by anyone:

```python
x = 300

def myfunc():
  print(x)

myfunc()

print(x)
```

### Global Keyword

If you need to create a global variable, but are stuck in the local scope, you can use the `global` keyword.

The `global` keyword makes the variable global.

#### Example

If you use the `global` keyword, the variable belongs to the global scope:

```python
def myfunc():
  global x
  x = 300

myfunc()

print(x)
```

Also, use the `global` keyword if you want to make a change to a global variable inside a function.

#### Example

To change the value of a global variable inside a function, refer to the variable by using the `global` keyword:

```python
x = 300

def myfunc():
  global x
  x = 200

myfunc()

print(x)
```
