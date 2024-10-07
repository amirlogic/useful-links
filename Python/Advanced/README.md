# Advanced Python

Beyond basics


## Environment variables

```python
import os
os.getenv("USER")
```

https://www.datacamp.com/tutorial/python-environment-variables


## with statement

```python
with open('file_path', 'w') as file:
    file.write('hello world !')
```


## BytesIO

```python
from io import BytesIO

file_bytes = BytesIO()

# Load data into file_bytes

file_bytes.seek(0)

print(file_bytes.getvalue())

```

## Generate temporary files and directories

```python
import tempfile

fp = tempfile.TemporaryFile()
fp.write(b'Hello world!')

# read data from file
fp.seek(0)
fp.read()
b'Hello world!'

# close the file, it will be removed
fp.close()
```










