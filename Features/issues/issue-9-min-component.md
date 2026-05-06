---
title: "Feature #9: Min component"
description: "Print the pixel with the minimum R, G, or B value in the output terminal."
Milestone: 2
Issue: 9
---

## Feature description

Print the pixel with the minimum R, G, or B value in the output terminal.
If multiple pixels are equals to the minimum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
name | min_component
Command | `-c min_component [R or G or B]`
Input  | an image 
output | `min_component [R or G or B] (x,y): value`

## Usage

```bash
freud.exe -f ./images/input/image.jpeg -c min_component R
or
freud.exe -f ./images/input/image.jpeg -c min_component G
or
freud.exe -f ./images/input/image.jpeg -c min_component B
```
## Output

```bash
min_component R (1098, 897): 11
or
min_component G (35, 1337): 0
or
min_component B (1078, 956): 0
```

## Describe tips for implementing feature

Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.
