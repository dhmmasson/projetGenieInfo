---
title: "Feature #4: Color of the first pixel on the second line"
description: "Print the color in RGB of the first pixel of the second line (coordinates 1,0) in the output terminal."
Milestone: 1
Issue: 4
---

## Feature description

Print the color in RGB of the first pixel of the second line (coordinates 1,0) in the output terminal. 
A possible prototype: 
```c
second_line(char *source_path);
``` 

Parameters|value
-|-
name         | second_line
Command | `-c second_line`
Input          | an image that has at least a height of 2 pixels 
output       | `second_line: R, G, B`<br> R, G, B are the integer values of the components in the range 0-255 

## Usage

```bash
freud.exe -f ./images/input/image.jpeg -c second_line 
```
## Output

```bash
second_line: 89, 139, 164
```
## Describe tips for implementing feature

Use the `data` from the function `read_image_data` from `estia-image.h`.
```c
int read_image_data(const char *filename, unsigned char **data, int *width, int *height, int *channel_count);
```
The components  R, G, B of the first pixel of the second line are located at 3*width, 3*width+1 and 3*width+2 in the data array(the first line has width pixel of 3 channels).
Read the [wiki](https://github.com/Estia-1a/projetGenieInfo_public/wiki/Image)
