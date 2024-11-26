# Pillow (PIL)

Image manipulation for Python


## Open



```im = Image.open("/path/to/image.jpg")```


## Bytes


```python

import io

pimg = Image.open(io.BytesIO(byte_data))

display(pimg)

```


