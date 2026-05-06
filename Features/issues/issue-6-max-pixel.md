---
title: "Feature #6: Max pixel"
description: "Print the pixel with the with the largest sum of RGB components in the output terminal."
Milestone: 2
Issue: 6
---

## Feature description

Print the pixel with the with the largest sum of RGB components in the output terminal. 
If multiple pixels are equals to the maximum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
name | max_pixel
Command | `-c max_pixel`
Input  | an image 
output | `max_pixel (x, y): R, G, B`

## Usage

```bash
freud.exe -f /images/input/image.jpeg -c max_pixel
```
## Output

```bash
max_pixel (528, 721): 255, 254, 255
```
## Describe tips for implementing feature

Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.
