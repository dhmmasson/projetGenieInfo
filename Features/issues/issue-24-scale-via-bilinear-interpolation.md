---
title: "Feature #24: Scale via bilinear interpolation"
description: "Scale the image (smaller or larger) via a smarter algorithm than nearest-neighbor."
Milestone: 5
Issue: 24
---

## Feature description

Scale the image (smaller or larger) via a smarter algorithm than nearest-neighbor.


Parameters|value
-|-
name         | scale_bilinear
Command | `-c scale_bilinear X` (with X the scale, such as 0.5 or 3)
Input          | an image 
output       | a new image `image_out.bmp` scaled by X from the input image

## Usage

```bash
./freud.exe -f images/input/image.jpeg -c scale_bilinear 3
```
## Output

A new image `image_out.bmp`, but 3 times larger than the input image



**Tips for implementing the feature**
Do not hesitate to look for resources online to find out how the algorithm works.

For instance (https://towardsdatascience.com/image-processing-image-scaling-algorithms-ae29aaa6b36c): 
![illustration of the algorithm](https://miro.medium.com/max/806/1*Vi4j20o_M14IJHeCgk2CaQ.png)

**Careful**: there are several online resources that do not cover _every_ aspects of the algorithm.
You might end up with black pixels and holes in your resulting image.


### Additional information

Example (`scale=0.5`):

|Input|Output|
|---|---|
|<img src="https://user-images.githubusercontent.com/14878561/171637527-c63fb289-c5a0-43d2-a04f-fe75ff7a51dd.jpeg" width="250px">|<img src="https://user-images.githubusercontent.com/14878561/171676133-9abb949d-a1d2-40d0-a47b-bf18b12575ba.jpg" width="125px">|
