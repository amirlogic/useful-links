# PyMuPDF

Facts on PDF files:
* Can contain not only text and images, but also videos, 3D models and can hold attached files
* Fonts can be included, but not always (licencing)


### Installation

```pip install --upgrade pymupdf```


### Basic Usage

```python
import pymupdf

doc = pymupdf.open("a.pdf") # open a document
```


## Text Extraction

```python
for page in doc: # iterate the document pages
                    text = page.get_text().encode("utf8") # get plain text (is in UTF-8)
                    print("Page text: ",text)
                    output += str(text) # write text of page

doc.close()
```



## xxx

```int()```




## String Methods






## Error Fixing

Pip SSL error https://www.youtube.com/watch?v=g9AeWgZJTZA



