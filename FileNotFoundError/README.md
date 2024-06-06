# FileNotFoundError - Trying to access files that do not exist

`FileNotFoundError` is raised when trying to open a file that does not exist. This error is a subclass of `OSError` and typically occurs with file operations like opening or deleting a file.

## Common Causes

1. **Incorrect File Path**: The specified file path does not exist or is incorrect.
2. **File Does Not Exist**: The file has been deleted or moved from its original location.
3. **Typo in File Name**: A typo in the file name or extension.
4. **Incorrect Working Directory**: The script is running in a different directory than expected.

## Example of the Error

```python
try:
    with open('non_existent_file.txt', 'r') as file:
        content = file.read()
except FileNotFoundError as e:
    print(f"Error: {e}")
```

Output:
```
Error: [Errno 2] No such file or directory: 'non_existent_file.txt'
```

## Solutions

### 1. Verify the File Path

Ensure that the file path is correct. You can use absolute paths to avoid issues with relative paths.

```python
file_path = '/path/to/your/file.txt'
try:
    with open(file_path, 'r') as file:
        content = file.read()
except FileNotFoundError as e:
    print(f"Error: {e}")
```

### 2. Check If the File Exists

Before attempting to open a file, check if it exists using the `os.path.exists()` method.

```python
import os

file_path = 'non_existent_file.txt'
if os.path.exists(file_path):
    with open(file_path, 'r') as file:
        content = file.read()
else:
    print(f"Error: {file_path} does not exist.")
```

### 3. Handle the Exception

Handle the `FileNotFoundError` exception to provide a user-friendly message or alternative action.

```python
file_path = 'non_existent_file.txt'
try:
    with open(file_path, 'r') as file:
        content = file.read()
except FileNotFoundError:
    print(f"Error: The file {file_path} was not found. Please check the path and try again.")
```

### 4. Create the File if It Doesn't Exist

In some cases, you might want to create the file if it doesn't exist.

```python
file_path = 'new_file.txt'
try:
    with open(file_path, 'r') as file:
        content = file.read()
except FileNotFoundError:
    with open(file_path, 'w') as file:
        file.write("This is a new file.")
    print(f"{file_path} was created.")
```

## Additional Resources

* [Official Python Documentation on FileNotFoundError](https://docs.python.org/3/library/exceptions.html#FileNotFoundError)
* [Real Python Guide on Reading and Writing Files](https://realpython.com/read-write-files-python/)
* [Stack Overflow](https://stackoverflow.com/questions/tagged/python)

Happy Coding! If you have any questions or need further assistance, feel free to contact us. Let's tackle these Python errors together and improve our coding skills!
