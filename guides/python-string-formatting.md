# Python String Formatting

To make sure a string will display as expected, we can format the result with the `format()` method.



### String format()

The `format()` method allows you to format selected parts of a string.

Sometimes there are parts of a text that you do not control, maybe they come from a database, or user input?

To control such values, add placeholders (curly brackets `{}`) in the text, and run the values through the `format()` method:

#### Example

Add a placeholder where you want to display the price:

```python
price = 49
txt = "The price is {} dollars"
print(txt.format(price))
```

You can add parameters inside the curly brackets to specify how to convert the value:

#### Example

Format the price to be displayed as a number with two decimals:

```python
txt = "The price is {:.2f} dollars"
```

### Multiple Values

If you want to use more values, just add more values to the format() method:

```python
print(txt.format(price, itemno, count))
```

And add more placeholders:

#### Example

```python
quantity = 3
itemno = 567
price = 49
myorder = "I want {} pieces of item number {} for {:.2f} dollars."
print(myorder.format(quantity, itemno, price))
```

### Index Numbers

You can use index numbers (a number inside the curly brackets `{0}`) to be sure the values are placed in the correct placeholders:

#### Example

```python
quantity = 3
itemno = 567
price = 49
myorder = "I want {0} pieces of item number {1} for {2:.2f} dollars."
print(myorder.format(quantity, itemno, price))
```

Also, if you want to refer to the same value more than once, use the index number:

#### Example

```python
age = 36
name = "John"
txt = "His name is {1}. {1} is {0} years old."
print(txt.format(age, name))
```

### Named Indexes

You can also use named indexes by entering a name inside the curly brackets `{carname}`, but then you must use names when you pass the parameter values `txt.format(carname = "Ford")`:

#### Example

```python
myorder = "I have a {carname}, it is a {model}."
print(myorder.format(carname = "Ford", model = "Mustang"))
```

## Python String format() Method

#### Example

Insert the price inside the placeholder, the price should be in fixed point, two-decimal format:

```python
txt = "For only {price:.2f} dollars!"
print(txt.format(price = 49))
```

### Definition and Usage

The `format()` method formats the specified value(s) and insert them inside the string's placeholder.

The placeholder is defined using curly brackets: {}. Read more about the placeholders in the Placeholder section below.

The `format()` method returns the formatted string.



### Syntax

_string_.format(_value1, value2..._)

### Parameter Values

| Parameter           | Description                                                                                                                                                                                                                                        |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _value1, value2..._ | <p>Required. One or more values that should be formatted and inserted in the string.<br><br>The values are either a list of values separated by commas, a key=value list, or a combination of both.<br><br>The values can be of any data type.</p> |



### The Placeholders

The placeholders can be identified using named indexes `{price}`, numbered indexes `{0}`, or even empty placeholders `{}`.

#### Example

Using different placeholder values:

```python
txt1 = "My name is {fname}, I'm {age}".format(fname = "John", age = 36)
txt2 = "My name is {0}, I'm {1}".format("John",36)
txt3 = "My name is {}, I'm {}".format("John",36)
```

#### Formatting Types

Inside the placeholders you can add a formatting type to format the result:

| `:<` | Left aligns the result (within the available space)                                                     |
| ---- | ------------------------------------------------------------------------------------------------------- |
| `:>` | Right aligns the result (within the available space)                                                    |
| `:^` | Center aligns the result (within the available space)                                                   |
| `:=` | Places the sign to the left most position                                                               |
| `:+` | Use a plus sign to indicate if the result is positive or negative                                       |
| `:-` | Use a minus sign for negative values only                                                               |
| `:`  | Use a space to insert an extra space before positive numbers (and a minus sign before negative numbers) |
| `:,` | Use a comma as a thousand separator                                                                     |
| `:_` | Use a underscore as a thousand separator                                                                |
| `:b` | Binary format                                                                                           |
| `:c` | Converts the value into the corresponding unicode character                                             |
| `:d` | Decimal format                                                                                          |
| `:e` | Scientific format, with a lower case e                                                                  |
| `:E` | Scientific format, with an upper case E                                                                 |
| `:f` | Fix point number format                                                                                 |
| `:F` | Fix point number format, in uppercase format (show `inf` and `nan` as `INF` and `NAN`)                  |
| `:g` | General format                                                                                          |
| `:G` | General format (using a upper case E for scientific notations)                                          |
| `:o` | Octal format                                                                                            |
| `:x` | Hex format, lower case                                                                                  |
| `:X` | Hex format, upper case                                                                                  |
| `:n` | Number format                                                                                           |
| `:%` | Percentage format                                                                                       |

Example

```python
#Use "%" to convert the number into a percentage format:

txt = "You scored {:%}"
print(txt.format(0.25))

#Or, without any decimals:

txt = "You scored {:.0%}"
print(txt.format(0.25))

```

```python
#Use "X" to convert the number into upper-case Hex format:

txt = "The Hexadecimal version of {0} is {0:X}"

print(txt.format(255))
```

```python
#Use "d" to convert a number, in this case a binary number, into decimal number format:

txt = "We have {:d} chickens."
print(txt.format(0b101))
```
