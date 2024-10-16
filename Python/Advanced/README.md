# Advanced Python

Beyond basics


## Environment variables

```python
import os
os.getenv("USER")
```

https://www.datacamp.com/tutorial/python-environment-variables


## with statement

"with" statement helps avoiding bugs and leaks by ensuring that a resource is properly released when the code using the resource is completely executed. The with statement is popularly used with file streams.

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

## CSV

Write CSV files 

```python
import csv
with open('eggs.csv', 'w', newline='') as csvfile:
    spamwriter = csv.writer(csvfile, delimiter=' ',
                            quotechar='|', quoting=csv.QUOTE_MINIMAL)
    spamwriter.writerow(['Spam'] * 5 + ['Baked Beans'])
    spamwriter.writerow(['Spam', 'Lovely Spam', 'Wonderful Spam'])
```

Read CSV files:

```python
import csv
with open('eggs.csv', newline='') as csvfile:
    spamreader = csv.reader(csvfile, delimiter=' ', quotechar='|')
    for row in spamreader:
        print(', '.join(row))
```

## Video

Image processing https://www.youtube.com/watch?v=oyqNdcbKhew



