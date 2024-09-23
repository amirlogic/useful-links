# PyMuPDF

Virtual Environments https://www.youtube.com/watch?v=0f3moPe_bhk



## Virtual Environments

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



