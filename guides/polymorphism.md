# Polymorphism

Polymorphism is one of the fundamental concepts in object-oriented programming (OOP) and is a key feature of Python. It allows objects of different classes to be treated as objects of a common superclass. In other words, it enables you to use a single interface to represent different types of objects.

Python achieves polymorphism through two main mechanisms: method overriding and method overloading.

**1. Method Overriding:**

Method overriding allows a subclass to provide a specific implementation of a method that is already defined in its superclass. This means that when you call a method on an object of the subclass, Python will execute the overridden method in the subclass rather than the one in the superclass. This is particularly useful for customizing behavior in derived classes while maintaining a consistent interface.

Here's an example:



```python
class Animal:
    def speak(self):
        pass
class Dog(Animal):
    def speak(self):
        return "Woof!"
class Cat(Animal):
    def speak(self):
        return "Meow!"
```

**Polymorphism in action**

```python
def animal_sound(animal):
    return animal.speak()
 
dog = Dog()
cat = Cat()
 
print(animal_sound(dog))  # Output: Woof!
print(animal_sound(cat))  # Output: Meow!
```

In this example, both the \`Dog\` and \`Cat\` classes inherit from the \`Animal\` class and override the \`speak\` method to provide their own implementations. The \`animal\_sound\` function demonstrates polymorphism by accepting objects of different subclasses of \`Animal\` and calling their \`speak\` methods.&#x20;

**2. Method Overloading (Duck Typing):**

Python doesn't support traditional method overloading, as seen in languages like Java or C++. Instead, it uses a concept called "Duck Typing." In Python, you can create functions that can work with different types of input as long as they support the required operations. This is known as "loose" or "ad hoc" polymorphism.

For example:

```python
def add(x, y):
    return x + y
    
print(add(5, 3))         # Output: 8
print(add("Hello, ", "world!"))  # Output: Hello, world!
```

In this case, the \`add\` function works with both integers and strings because Python checks the compatibility of the provided arguments at runtime, rather than during compilation.
