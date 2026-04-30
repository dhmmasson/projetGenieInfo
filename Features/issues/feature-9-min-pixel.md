# Feature #9: Min pixel

- State: open
- Milestone: Milestone 2: Statistics
- Labels: export, statistics
- Assignees: None
- Created: 2022-06-02T12:36:25Z
- Updated: 2022-06-14T07:17:34Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/9

## Description

**Feature description**
Print the pixel with the with the smallest sum of RGB components in the output terminal. 
If multiple pixels are equals to the minimum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
Name | min_pixel
Command | `-c min_pixel`
Input  | an image 
output | `min_pixel (x, y): R, G, B`

**Usage**
```bash
freud.exe -f ./images/input/image.jpeg -c min_pixel
```
**Output**
```bash
min_pixel (35, 1337): 14, 0, 0
```
**Describe tips for implementing feature**
Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.
