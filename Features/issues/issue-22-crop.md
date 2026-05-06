---
title: "Feature #22: Crop"
description: "Crop the image. The result is the intersection of a cropping box (defined by a it center and dimension) and the original image"
Milestone: 5
Issue: 22
---

## Feature description

Crop the image. The result is the intersection of a cropping box (defined by a it center and dimension) and the original image

Parameters|value
-|-
name         | scale_crop
Command | `-c scale_crop center_x center_y width height`
Input          | an image 
output       | a new image `image_out.bmp` based on the input image with a box (size = `width`px, `height`px) centered around the pixel with coordinates `(center_x, center_y)` 

## Usage

```bash
./freud.exe -f images/input/image.jpeg -c scale_crop 500 600 300 400
```
## Output

A new image `image_out.bmp` based on the input image with a box (size = 300×400px) centered around the pixel with coordinates (500, 600). 


**Tips for implementing the feature**
Careful to the size of the box!
Make sure that even if the boundaries exit the original image (e.g., `center_x = 700`, `width=400`, `original_width=1000`), the resulting image is in the correct format and size. 



### Additional information

Example:
`freud.exe -f images/input/image.jpeg -c scale_crop 200 1000 200 400`

|Input | Output|
|---|---|
<img src="https://user-images.githubusercontent.com/14878561/171637527-c63fb289-c5a0-43d2-a04f-fe75ff7a51dd.jpeg" height="250px">|<img src="https://user-images.githubusercontent.com/14878561/172628943-221a0551-3fac-456e-9ea8-02fe025510ba.jpg" height="250px">
