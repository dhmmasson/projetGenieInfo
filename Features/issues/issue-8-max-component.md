---
title: "Feature #8: Max component"
description: "Print the pixel with the maximum R, G, or B value in the output terminal."
Milestone: 2
Issue: 8
---

## Feature description

Print the pixel with the maximum R, G, or B value in the output terminal.
If multiple pixels are equals to the maximum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
name | max_component
Command | `-c max_component [R or G or B]`
Input  | an image 
output | `max_component [R or G or B] (x,y): value`

## Usage

```bash
freud.exe -f ./images/input/image.jpeg -c max_component R
or
freud.exe -f ./images/input/image.jpeg -c max_component G
or
freud.exe -f ./images/input/image.jpeg -c max_component B
```
## Output

```bash
max_component R (528, 721): 255
or
max_component G (528, 721): 254
or
max_component B (528, 721): 255
```

## Describe tips for implementing feature

Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.
