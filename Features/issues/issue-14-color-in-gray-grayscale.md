---
title: "Feature #14: Color in gray (grayscale)"
description: "Transform the image to keep only a gray version (an average of the R, G, B components for each pixel)."
Milestone: 3
Issue: 14
---

## Feature description

Transform the image to keep only a gray version (an average of the R, G, B components for each pixel).

Parameters|value
-|-
name         | color_gray
Command | `-c color_gray`
Input          | an image 
output       | a new `image_out.bmp` that keeps only a gray version of the input image

## Usage

```bash
./freud.exe -f images/input/image.jpeg -c color_gray
```
## Output

A new image `image_out.bmp` as a gray version of the input image

## Describe tips for implementing feature

Simply compute the average value of each pixel like the pseudo-code below.

```c
unsigned char value = (getPixel(x, y)->R + getPixel(x, y)->G + getPixel(x, y)->B) / 3
```

The resulting image will lake luminosity.

## Describe tips for implementing feature

Use write_image_data from <estia-image.h> to create new image with the new values.

```c
/**
 * Writes into an image file
 * @param[in] filename Name of the file to be written into
 * @param[in] data Reference to the pixel array to be written
 * @param[in] width Width of the image
 * @param[in] height Height of the image
 * @return 0 on failure and non-0 on success.
 */
int write_image_data(const char *filename, unsigned char *data, int width, int height);
```



### Additional information

Example:

|Input|Output|
|---|---|
| | |
