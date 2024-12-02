# PyMuPDF

Facts on PDF files:
* Can contain not only text and images, but also videos, 3D models and can hold attached files
* Fonts can be included, but not always (licencing)
* In PDF documents, everything is measured using “Point”. In the PDF world, 1 point = 1/72 inch
* Unlike a raster image, in which the origin is located at the top left corner, the PDF document's origin is (by default) located at the bottom left corner.

A PDF document also contains page boundaries also known as “boxes”. The MediaBox is used to specify the width and height of the page. For the average user, this probably equals the actual page size.
The MediaBox is mandatory and is the largest page box in a PDF document. The CropBox is optional and defines the region to which the page content is to clipped, it is used for displaying and printing. It can have the same size as the MediaBox, but if it is smaller, what is outside the CropBox boundaries, won’t be visible.


### Installation

```pip install --upgrade pymupdf```


### Basic Usage

```python
import pymupdf

doc = pymupdf.open("a.pdf") # open a document
```


### Working with pages

```python

page = doc.load_page(pno)  # loads page number 'pno' of the document (0-based)

# or

page = doc[pno]

```


### Text Extraction

```python
for page in doc: # iterate the document pages
  text = page.get_text().encode("utf8") # get plain text (is in UTF-8)
  print("Page text: ",text)

doc.close()
```

### Image extraction

```python
doc.extract_image(xref)
```

There are two ways for getting the xref:

```python

images = page.get_images()

for img in images:
    imgdata = doc.extract_image(img[0])

```

```python

lenXREF = doc.xref_length()

for xref in range(1, lenXREF):
    
    if(doc.xref_get_key(xref, "Subtype")[1] == "/Image"):

        imgdata = doc.extract_image(xref)

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




## Tutorials


### Images

https://pymupdf.readthedocs.io/en/latest/recipes-images.html

https://artifex.com/blog/pymupdf-explored-image-handling-in-pdf




### RAG - LLM

https://artifex.com/blog/building-a-multimodal-llm-application-with-pymupdf4llm

https://artifex.com/blog/rag-llm-and-pdf-enhanced-text-extraction

Chunking Levels: https://github.com/FullStackRetrieval-com/RetrievalTutorials/blob/main/tutorials/LevelsOfTextSplitting/5_Levels_Of_Text_Splitting.ipynb






