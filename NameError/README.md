# NameError - Errors Due to Undefined Variables or Functions

A `NameError` in Python occurs when you try to use a variable or function name that has not been defined. This error is common for beginners and can be easily fixed once you understand the cause.

## Common Causes

1. **Misspelled Variable or Function Names**: The most common cause of a `NameError` is a typo in the variable or function name.
2. **Using Variables Before Declaration**: Referencing a variable before it has been assigned a value.
3. **Scope Issues**: Trying to access variables outside their scope.
4. **Imported Modules**: Forgetting to import a module or using incorrect module names.

## Scenarios and Solutions

### 1. Misspelled Variable or Function Names

**Example:**
```python
my_var = 10
print(my_vr)
```
**Error:**
```plaintext
NameError: name 'my_vr' is not defined
```
**Solution:** Ensure that the variable name is spelled correctly.
```python
my_var = 10
print(my_var)
```

### 2. Using Variables Before Declaration

**Example:**
```python
print(my_var)
my_var = 10
```
**Error:**
```plaintext
NameError: name 'my_var' is not defined
```
**Solution:** Declare the variable before using it.
```python
my_var = 10
print(my_var)
```

### 3. Scope Issues

**Example:**
```python
def my_function():
    my_var = 10

print(my_var)
```
**Error:**
```plaintext
NameError: name 'my_var' is not defined
```
**Solution:** Ensure that the variable is accessible within the scope it is being used.
```python
def my_function():
    my_var = 10
    print(my_var)

my_function()
```

### 4. Imported Modules

**Example:**
```python
print(math.pi)
```
**Error:**
```plaintext
NameError: name 'math' is not defined
```
**Solution:** Import the necessary module before using it.
```python
import math
print(math.pi)
```

## Additional Tips

1. **Check Spelling**: Always double-check the spelling of your variable and function names.
2. **Use IDEs/Linters**: Integrated Development Environments (IDEs) and linters can help catch these errors before running the code.
3. **Print Statements**: Use print statements to debug and ensure variables are defined before they are used.

## More Resources

- [Python Official Documentation on NameError](https://docs.python.org/3/library/exceptions.html#NameError)
- [Stack Overflow - Python NameError Questions](https://stackoverflow.com/questions/tagged/nameerror)

Feel free to explore and ask questions if you need further assistance with `NameError` or any other Python errors. Happy coding!
