# JSON

JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write. It is also easy for machines to parse and generate. In Python, you can work with JSON data using the built-in \`json\` module.

JSON Syntax

JSON data is represented as key-value pairs, similar to Python dictionaries. JSON keys are always strings, and values can be strings, numbers, objects, arrays, \`true\`, \`false\`, or \`null\`. Here's a basic example of JSON data:

`{`

&#x20; `"name": "John",`

&#x20; `"age": 30,`

&#x20; `"city": "New York"`

`}`

JSON in Python

To work with JSON in Python, you need to import the \`json\` module. Here's how you can encode Python data into JSON:

```python
import json
# Create a Python dictionary
data = {
    "name": "John",
    "age": 30,
    "city": "New York"
}

```

```python
# Encode the dictionary as JSON
json_data = json.dumps(data)
print(json_data)

```

```
The `json.dumps()` function takes a Python object and converts it into a JSON string.
```

Decoding JSON You can also decode JSON data in Python using the `json.loads()` function. Here's an example:

```python
import json
# JSON data as a string
json_data = '{"name": "John", "age": 30, "city": "New York"}'
# Decode JSON into a Python dictionary
data = json.loads(json_data)
print(data)

```

The `json.loads()` function takes a JSON string and converts it into a Python object.

**Working with JSON Files**&#x20;

JSON is commonly used for data storage and exchange. You can read and write JSON data from/to files in Python. Here's an example of reading JSON data from a file



```python
import json
# Read JSON data from a file
with open("data.json", "r") as file:
    data = json.load(file)
print(data)

```

And here's an example of writing JSON data to a file:

```python
import json
# Python data to be written as JSON
data = {
    "name": "Alice",
    "age": 25,
    "city": "San Francisco"
}

```

```python
# Write JSON data to a file
with open("output.json", "w") as file:
    json.dump(data, file)

```

**Handling JSON Errors**

Handling JSON Errors When working with JSON data, it's important to handle errors gracefully. JSON decoding can raise `json.JSONDecodeError` if the input is not valid JSON. Here's how to handle it:

```python
import json
json_data = 'invalid json'
try:
    data = json.loads(json_data)
except json.JSONDecodeError as e:
    print("JSON decoding error:", e)

```
