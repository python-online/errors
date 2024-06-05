# IndentationError: Issues Related to Improper Indentation

An `IndentationError` in Python is raised when the code contains inconsistent or incorrect indentation. Python relies heavily on indentation to define the structure and flow of the program, particularly within loops, functions, classes, and conditional statements.

## Common Causes

1. **Mixed Spaces and Tabs**: Using a combination of spaces and tabs for indentation within the same block of code.
2. **Incorrect Indentation Level**: Indenting a line of code at an incorrect level relative to its surrounding lines.
3. **Missing Indentation**: Forgetting to indent the block of code that follows a colon (`:`) at the end of statements like `if`, `for`, `while`, `def`, and `class`.

## Example and Solution

### Example 1: Mixed Spaces and Tabs

#### Code with Error:
```python
def example_function():
    if True:
        print("This line uses spaces")
		print("This line uses a tab")
```

#### Error Message:
```
IndentationError: unindent does not match any outer indentation level
```

#### Solution:
Use either spaces or tabs consistently for indentation. The Python style guide (PEP 8) recommends using 4 spaces per indentation level.

```python
def example_function():
    if True:
        print("This line uses spaces")
        print("This line also uses spaces")
```

### Example 2: Incorrect Indentation Level

#### Code with Error:
```python
def example_function():
    if True:
        print("This line is correctly indented")
      print("This line has incorrect indentation")
```

#### Error Message:
```
IndentationError: unindent does not match any outer indentation level
```

#### Solution:
Ensure that all lines within the same block of code have the same indentation level.

```python
def example_function():
    if True:
        print("This line is correctly indented")
        print("This line is also correctly indented")
```

### Example 3: Missing Indentation

#### Code with Error:
```python
def example_function():
    if True:
    print("This line should be indented")
```

#### Error Message:
```
IndentationError: expected an indented block
```

#### Solution:
Indent the block of code following a statement that ends with a colon (`:`).

```python
def example_function():
    if True:
        print("This line is now correctly indented")
```

## Tips to Avoid Indentation Errors

1. **Consistent Use of Spaces**: Configure your text editor to insert spaces when you press the Tab key. Most modern editors have this feature.
2. **Visible Whitespace**: Enable visible whitespace in your editor to easily spot tabs and spaces.
3. **Automatic Indentation**: Use an IDE or code editor that provides automatic indentation and code formatting features.
4. **Linting Tools**: Use linting tools like `pylint` or `flake8` to check for indentation errors and other style issues.

## Additional Resources

- [Python Indentation Guide](https://docs.python.org/3/reference/lexical_analysis.html#indentation)
- [PEP 8 - Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/#indentation)

By understanding the common causes and solutions for `IndentationError`, you can write cleaner and more error-free Python code. If you encounter an `IndentationError`, review your code carefully to ensure consistent and correct indentation throughout.
