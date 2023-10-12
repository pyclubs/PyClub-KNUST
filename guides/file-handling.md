# File Handling

File handling is an essential part of any programming language, allowing you to read and write data to and from files. In Python, you can perform various file operations using built-in functions and methods. This tutorial will cover the basics of file handling in Python.

**Opening and Closing Files**

Before you can read from or write to a file, you need to open it. Python provides the \`open()\` function for this purpose. You can specify the file's name and the mode in which you want to open it (read, write, or append).

`file = open("example.txt", "r")`

**Open a file for writing (creates a new file if it doesn't exist)**

`file = open("example.txt", "w")`

**Open a file for appending (creates a new file if it doesn't exist)**

`file = open("example.txt", "a")`

After performing file operations, it's essential to close the file using the \`close()\` method to free up system resources.

`file.close()`

**Reading Files**

To read the contents of a file, you can use various methods provided by Python. The most common method is \`read()\`, which reads the entire file content

`file = open("example.txt", "r")`

`content = file.read()`

`print(content)`

`file.close()`

You can also read a file line by line using a \`for\` loop.

`file = open("example.txt", "r")`

`for line in file:`

&#x20;   `print(line)`

`file.close()`

Writing to Files

To write data to a file, you can use the \`write()\` method. Remember to open the file in write or append mode.

`file = open("example.txt", "w")`

`file.write("Hello, World!")`

`file.close()`

If you want to write multiple lines, you can use a loop or write a list of strings to the file.

`lines = ["Line 1", "Line 2", "Line 3"]`

`file = open("example.txt", "w")`

`file.writelines(lines)`

`file.close()`

**Closing Files Automatically (with \`with\`)**

Python's \`with\` statement makes it easier to work with files, as it automatically closes the file when the block is exited, even if an exception occurs.

`with open("example.txt", "r") as file:`

&#x20;   `content = file.read()`

&#x20;   `print(content)`

&#x20;File is automatically closed when the block is exited

&#x20;File Modes

Here are some commonly used file modes:

\- \`'r'\`: Read (default mode). Opens the file for reading.

\- \`'w'\`: Write. Opens the file for writing. Creates a new file or overwrites an existing one.

\- \`'a'\`: Append. Opens the file for writing, but appends to the end of the file.

\- \`'b'\`: Binary mode. Used in combination with other modes to read or write binary data.

\- \`'x'\`: Exclusive creation. Creates a new file but raises an error if it already exists.

&#x20;Exception Handling

When working with files, it's a good practice to use exception handling to deal with potential errors, such as file not found or permission issues.

`try:`

&#x20;   `file = open("example.txt", "r")`

`# File operations here`

`except FileNotFoundError:`

&#x20;   `print("The file does not exist.")`

`except PermissionError:`

&#x20;   `print("Permission denied.")`

`finally:`

&#x20;   `file.close()  # Always close the file, even in case of an exception`

&#x20;

In Python, you can read the contents of a file using several methods, depending on your specific needs. Here are some commonly used methods to read the contents of a file:

1\. \`read()\` Method: This method reads the entire content of the file as a single string.

&#x20;  `with open("example.txt", "r") as file:`

&#x20;      `content = file.read()`

&#x20;      `print(content)`

2\. \`readline()\` Method: This method reads the file one line at a time. You can use it in a loop to read the entire file line by line.

&#x20;`with open("example.txt", "r") as file:`

&#x20;      `for line in file:`

&#x20;          `print(line)`

3\. readlines()\` Method: This method reads all the lines of the file and returns them as a list of strings, with each line as an element in the list.

&#x20;`with open("example.txt", "r") as file:`

&#x20;      `lines = file.readlines()`

&#x20;      `for line in lines:`

&#x20;          `print(line)`

4\. Reading N Characters: You can read a specific number of characters from the file using the \`read(N)\` method, where \`N\` is the number of characters to read.

&#x20;  with open("example.txt", "r") as file:

&#x20;      partial\_content = file.read(50)  # Read the first 50 characters

&#x20;      print(partial\_content)

5\. Iterating Over \`file\` Object: You can also iterate over the \`file\` object itself. This is similar to using \`readline()\` but more memory-efficient, especially for large files.

&#x20;  with open("example.txt", "r") as file:

&#x20;    `for line in file:`

&#x20;          `print(line)`

6\. Using \`for\` Loop with \`readlines()\`: You can read lines from the file into a list using \`readlines()\` and then iterate over the list with a \`for\` loop.

&#x20;**with open("example.txt", "r") as file:**

&#x20;      **lines = file.readlines()**

&#x20;      **for line in lines:**

&#x20;          **print(line)**
