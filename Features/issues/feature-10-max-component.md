# Feature #10: Max component

- State: open
- Milestone: Milestone 2: Statistics
- Labels: export, statistics
- Assignees: None
- Created: 2022-06-02T13:00:01Z
- Updated: 2022-06-22T08:08:18Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/10

## Description

**Feature description**
Print the pixel with the maximum R, G, or B value in the output terminal.
If multiple pixels are equals to the maximum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
name | max_component
Command | `-c max_component [R or G or B]`
Input  | an image 
output | `max_component [R or G or B] (x,y): value`

**Usage**
```bash
freud.exe -f ./images/input/image.jpeg -c max_component R
or
freud.exe -f ./images/input/image.jpeg -c max_component G
or
freud.exe -f ./images/input/image.jpeg -c max_component B
```
**Output**
```bash
max_component R (528, 721): 255
or
max_component G (528, 721): 254
or
max_component B (528, 721): 255
```

**Describe tips for implementing feature**
Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.

