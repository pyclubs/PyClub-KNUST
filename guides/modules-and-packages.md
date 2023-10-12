# Modules and Packages

### What is a Module?

Consider a module to be the same as a code library.

A file containing a set of functions you want to include in your application.

***

### Create a Module

To create a module just save the code you want in a file with the file extension `.py`:

#### Example

Save this code in a file named `mymodule.py`

```python
def greeting(name):
  print("Hello, " + name)
```

### Use a Module

Now we can use the module we just created, by using the `import` statement:

#### Example

Import the module named mymodule, and call the greeting function:

```python
import mymodule

mymodule.greeting("Jonathan")
```

{% hint style="info" %}
When using a function from a module, use the syntax: _module\_name.function\_name_.
{% endhint %}

### Variables in Module

The module can contain functions, as already described, but also variables of all types (arrays, dictionaries, objects etc):

#### Example

Save this code in the file `mymodule.py`

```python
person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```

#### Example

Import the module named mymodule, and access the person1 dictionary:

```python
import mymodule

a = mymodule.person1["age"]
print(a)
```

### Naming a Module

You can name the module file whatever you like, but it must have the file extension `.py`

### Re-naming a Module

You can create an alias when you import a module, by using the `as` keyword:

#### Example

Create an alias for `mymodule` called `mx`:

```python
import mymodule as mx

a = mx.person1["age"]
print(a)
```

### Built-in Modules

There are several built-in modules in Python, which you can import whenever you like.

#### Example

Import and use the `platform` module:

```python
import platform

x = platform.system()
print(x)
```

### Import From Module

You can choose to import only parts from a module, by using the `from` keyword.

#### Example

The module named `mymodule` has one function and one dictionary:

```python
def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```

#### Example

Import only the person1 dictionary from the module:

```python
from mymodule import person1

print (person1["age"])
```

{% hint style="info" %}
When importing using the `from` keyword, do not use the module name when referring to elements in the module. Example: `person1["age"]`, **not** `mymodule.person1["age"]`
{% endhint %}
