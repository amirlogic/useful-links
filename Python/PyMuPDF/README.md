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


### Text Extraction

```python
for page in doc: # iterate the document pages
  text = page.get_text().encode("utf8") # get plain text (is in UTF-8)
  print("Page text: ",text)

doc.close()
```

### Save page as pixmap

```python
page = doc[pgnum]

pix = page.get_pixmap()

pix.save("page-%i.png" % page.number)

print("pixmap saved")
```

### Insert Image

```python
doc = pymupdf.open() # some new or existing PDF document

rect = pymupdf.Rect(0, 0, 100, 100) 

img = open(filename, "rb").read()

img_xref = 0 

page = doc.insert_page(-1) #doc[pgnum]

pg = doc[0]

img_xref = pg.insert_image(rect, stream=img,
                 xref=img_xref )

print("Image inserted: ", filename)
```

### Tables

```python
for page in doc:
  tbls = page.find_tables()
  print("Tables found: ",len(tbls.tables))
                   
  if(len(tbls.tables)>0):
    print("This page contains tables")
    for wt in tbls.tables:
      cr = wt.extract()
      print(cr)
                            
doc.close()

```

Data can also be converted to Pandas Dataframe or Excel file




## String Methods










