---
title: "Posts Guide and Format"
date: 2020-09-17T23:18:13+03:00
draft: false
---
I am one person who is careful when it comes to order and
perfection and such has neccessiated me to create this manual
to help me improve my projects writing and formarting

## Images Format & Size Requirements

### Image Tools

GIMP is a powerful raster image editing. 

```
sudo pacman -S gimp imagemagick
```

### Idenify image size
```
identify -format "%wx%h" image.jpg
```
### Resize ignoring aspect ratio
```
convert image.png -resize 100x100! image_resized.png
```
### Resize keeping aspect ratio
```
convert image.png -resize 100x100 image_resized_aspect.png
```
### Resize an image
```
convert image.jpg -resize 600x400\> image_resized.jpg
```
### Confirm that the image has been resized
```
identify -format "%wx%h" image_resized.jpg
```
### Resize using mogrify(This will affect original file so make sure you have a backup)
```
mogrify -resize 100x100 original.png
```
### Resize image to width 25, keeping aspect ratio
```
convert -geometry 25x src/image1.png out/image1.png
```
### Resize image to height 25, keeping aspect ratio
```
convert -geometry x25 src/image1.png out/image1.png
```
### Concatenate images horizontally
```
convert +append src/image1.png src/image2.png out/image12horiz.png
```
### Concatenate images vertically
```
convert -append src/image1.png src/image2.png out/image12vert.png
```
In order to render the site well, all images should be less than
150kB in size and resolution of 1024X768




## Checklist Before Publishing

This is my checklist before the post goes live

* Grammar and Spellcheck.
* Fullstops and commas.
* Tags.
* Code is highlighted well.
* Ensure that all links are working.
* Ensure that all sources are mentioned in the arknowledges section.
* Ensure that the post is available as a PDF and links are okay.
