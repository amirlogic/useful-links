# ImageMagick

Command line image editing https://imagemagick.com

## Resize image
```bash
 magick convert image.png -resize 960x540 image_resized.png
```



## Masking
```bash
convert original.png -matte mask.png -compose DstIn -composite output.png
```

## Turn white color to transparent

```bash
 magick convert source.png -fuzz 20% -transparent white result.png
```

## Label

https://usage.imagemagick.org/text/

```bash
magick -background lightblue -fill blue \
          -font Candice -pointsize 72 label:Anthony \
          label.gif
```


