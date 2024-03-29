# Inheritance

### Python Inheritance

Inheritance allows us to define a class that inherits all the methods and properties from another class.

**Parent class** is the class being inherited from, also called base class.

**Child class** is the class that inherits from another class, also called derived class.

***

### Create a Parent Class

Any class can be a parent class, so the syntax is the same as creating any other class:

#### Example

Create a class named `Person`, with `firstname` and `lastname` properties, and a `printname` method:

```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:

x = Person("John", "Doe")
x.printname()
```

Create a Child Class

To create a class that inherits the functionality from another class, send the parent class as a parameter when creating the child class:

#### Example

Create a class named `Student`, which will inherit the properties and methods from the `Person` class:

```python
class Student(Person):
  pass
```

{% hint style="info" %}
Use the `pass` keyword when you do not want to add any other properties or methods to the class.
{% endhint %}

Now the Student class has the same properties and methods as the Person class.

#### Example

Use the `Student` class to create an object, and then execute the `printname` method:\


```python
x = Student("Mike", "Olsen")
x.printname()
```

### Add the \_\_init\_\_() Function

So far we have created a child class that inherits the properties and methods from its parent.

We want to add the `__init__()` function to the child class (instead of the `pass` keyword).

{% hint style="info" %}
The `__init__()` function is called automatically every time the class is being used to create a new object.
{% endhint %}

#### Example

Add the `__init__()` function to the `Student` class:

```
class Student(Person):
  def __init__(self, fname, lname):
    #add properties etc.
```

When you add the `__init__()` function, the child class will no longer inherit the parent's `__init__()` function.
