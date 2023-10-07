# Pip

### What is PIP?

PIP is a package manager for Python packages, or modules if you like.

**Note:** If you have Python version 3.4 or later, PIP is included by default.



### What is a Package?

A package contains all the files you need for a module.

Modules are Python code libraries you can include in your project.

\
nstall PIP

If you do not have PIP installed, you can download and install it from this page: [https://pypi.org/project/pip/](https://pypi.org/project/pip/)



### Download a Package

Downloading a package is very easy.

Open the command line interface and tell PIP to download the package you want.

Navigate your command line to the location of Python's script directory, and type the following:

#### Example

Download a package named "camelcase":

`C:\Users\`_`Your Name`_`\AppData\Local\Programs\Python\Python36-32\Scripts>pip install camelcase`

Now you have downloaded and installed your first package!





### Using a Package

Once the package is installed, it is ready to use.

Import the "camelcase" package into your project.

#### Example

```python
//Import and use "camelcase":
import camelcase

c = camelcase.CamelCase()

txt = "hello world"

print(c.hump(txt))
```

### Find Packages

Find more packages at [https://pypi.org/](https://pypi.org/).



### Remove a Package

Use the `uninstall` command to remove a package:

#### Example

Uninstall the package named "camelcase":

`C:\Users\`_`Your Name`_`\AppData\Local\Programs\Python\Python36-32\Scripts>pip uninstall camelcase`

### List Packages

Use the `list` command to list all the packages installed on your system:

#### Example

List installed packages:

`C:\Users\`_`Your Name`_`\AppData\Local\Programs\Python\Python36-32\Scripts>pip list`
