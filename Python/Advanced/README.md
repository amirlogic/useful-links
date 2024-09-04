# Advanced Python

Beyond basics

## BytesIO

```python
from io import BytesIO

file_bytes = BytesIO()


```

### Generate temporary files and directories

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










