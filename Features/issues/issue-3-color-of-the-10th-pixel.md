---
title: "Feature #3: Color of the 10th pixel"
description: "Print the color in RGB of the tenth pixel (coordinates 9, 0) in the output terminal."
Milestone: 1
Issue: 3
---

## Feature description

Print the color in RGB of the tenth pixel (coordinates 9, 0) in the output terminal.
A possible prototype: 
```c
void tenth_pixel (char *source_path);
```

Parameters|value
-|-
name         | tenth_pixel
Command | `-c tenth_pixel`
Input          | an image that has at least a width of 10 pixels 
output       | `tenth_pixel: R, G, B`<br> R, G, B are the integer values of the components in the range 0-255 

## Usage

```bash
freud.exe -f ./images/input/image.jpeg -c tenth_pixel 
```
## Output

```bash
tenth_pixel: 86, 136, 161
```
## Describe tips for implementing feature

Use the `data` from the function `read_image_data` from `<estia-image.h>`.
```c
int read_image_data(const char *filename, unsigned char **data, int *width, int *height, int *channel_count);
```
The components  R, G, B of the tenth pixel are the located at 27, 28 and 29 in the data array. (the first pixel is index 0, so the tenth is index 9).
Read the [wiki](https://github.com/Estia-1a/projetGenieInfo_public/wiki/Image) 
Call `tenth_pixel` in `src/main.c`. See the `helloworld` example to correctly call the function.
