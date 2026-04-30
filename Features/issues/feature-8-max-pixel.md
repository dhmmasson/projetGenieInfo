# Feature #8: Max pixel

- State: open
- Milestone: Milestone 2: Statistics
- Labels: export, statistics
- Assignees: None
- Created: 2022-06-02T12:35:28Z
- Updated: 2022-06-14T07:17:14Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/8

## Description

**Feature description**
Print the pixel with the with the largest sum of RGB components in the output terminal. 
If multiple pixels are equals to the maximum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
name | max_pixel
Command | `-c max_pixel`
Input  | an image 
output | `max_pixel (x, y): R, G, B`

**Usage**
```bash
freud.exe -f /images/input/image.jpeg -c max_pixel
```
**Output**
```bash
max_pixel (528, 721): 255, 254, 255
```
**Describe tips for implementing feature**
Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.
