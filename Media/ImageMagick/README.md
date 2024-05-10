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
