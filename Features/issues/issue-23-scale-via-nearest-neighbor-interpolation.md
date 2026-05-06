---
title: "Feature #23: Scale via Nearest-neighbor interpolation"
description: "Scale the image (smaller or larger)"
Milestone: 5
Issue: 23
---

## Feature description

Scale the image (smaller or larger)


Parameters|value
-|-
name         | scale_nearest
Command | `-c scale_nearest X` (with X the scale, such as 0.5 or 3)
Input          | an image 
output       | a new image `image_out.bmp` scaled by X from the input image

## Usage

```bash
./freud.exe -f images/input/image.jpeg -c scale_nearest 3
```
## Output

A new image `image_out.bmp` 3 times larger than the input image



**Tips for implementing the feature**
Do not hesitate to look for resources online to find out how the algorithm works.

For instance (https://towardsdatascience.com/image-processing-image-scaling-algorithms-ae29aaa6b36c): 
![illustration of the algorithm](https://miro.medium.com/max/524/1*Zse7Mxw8J0Q2L3fBvqtuJA.png)


### Additional information

Example (`scale=0.5`):

|Input|Output|
|---|---|
|<img src="https://user-images.githubusercontent.com/14878561/171637527-c63fb289-c5a0-43d2-a04f-fe75ff7a51dd.jpeg" width="250px">|<img src="https://user-images.githubusercontent.com/14878561/171674997-ca9477eb-84d7-4a51-9cab-66ace63437e3.jpg" width="125px">|
