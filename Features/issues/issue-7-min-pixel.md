---
title: "Feature #7: Min pixel"
description: "Print the pixel with the with the smallest sum of RGB components in the output terminal."
Milestone: 2
Issue: 7
---

## Feature description

Print the pixel with the with the smallest sum of RGB components in the output terminal. 
If multiple pixels are equals to the minimum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
Name | min_pixel
Command | `-c min_pixel`
Input  | an image 
output | `min_pixel (x, y): R, G, B`

## Usage

```bash
freud.exe -f ./images/input/image.jpeg -c min_pixel
```
## Output

```bash
min_pixel (35, 1337): 14, 0, 0
```
## Describe tips for implementing feature

Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.
