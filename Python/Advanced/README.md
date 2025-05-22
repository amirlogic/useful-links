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


## Write file

```python
f = open("filename.ext", "a")
f.write("File content")
f.close()
```
"a" means appending, adds content to an existing file (or create if does not exists)

Use "wb" to write bytes into a file


## Pathlib

### List all files:

```python

mydir = pathlib.Path('/some/path')

for item in mydir.iterdir():
    if(item.is_file()):
        print(item)
```

https://www.youtube.com/watch?v=UcKkmwaRbsQ

https://www.youtube.com/watch?v=yxa-DJuuTBI


### More


Current dir: `Path.cwd()`

Home dir: `Path.home()`

Parent: `Path.parent`

Join: `Path("/") / "path" / "to" / "some" / "file.txt"`


### Extract

Extension: `Path.suffix` (includes dot)

Filename without ext.: `Path.stem`


## Base64

```python
import base64

sample_string = "Some text"
sample_string_bytes = sample_string.encode("ascii")

base64_bytes = base64.b64encode(sample_string_bytes)
base64_string = base64_bytes.decode("ascii")

print(f"Encoded string: {base64_string}")
```


## BytesIO

```python
from io import BytesIO

file_bytes = BytesIO()

# Load data into file_bytes

file_bytes.seek(0)

print(file_bytes.getvalue())

```

## JSON

Parse

```python
y = json.loads(x)
```

Stringify

```python
y = json.dumps(x)
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

## Pydantic

Introduction: https://www.youtube.com/watch?v=502XOB0u8OY


## GUI

https://wxpython.org/




## Video

Image processing https://www.youtube.com/watch?v=oyqNdcbKhew



