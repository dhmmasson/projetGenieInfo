---
title: "Feature #18: Rotate anti-clockwise 90°"
description: "Transform the image with a rotation effect: 90° anti-clockwise rotation."
Milestone: 4
Issue: 18
---

## Feature description

Transform the image with a rotation effect: 90° anti-clockwise rotation.

Parameters|value
-|-
name         | rotate_acw
Command | `-c rotate_acw`
Input          | an image 
output       | a new image `image_out.bmp` that is a 90° anti-clockwise rotation of the input image

## Usage

```bash
./freud.exe -f images/input/image.jpeg -c rotate_acw 
```
## Output

A new image `image_out.bmp` that is a 90° anti-clockwise rotation of the input image
