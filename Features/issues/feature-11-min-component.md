# Feature #11: Min component

- State: open
- Milestone: Milestone 2: Statistics
- Labels: export, statistics
- Assignees: None
- Created: 2022-06-02T13:01:14Z
- Updated: 2022-06-22T08:07:44Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/11

## Description

**Feature description**
Print the pixel with the minimum R, G, or B value in the output terminal.
If multiple pixels are equals to the minimum, return the first pixel encountered (i.e. min (x,y)).

Parameters|value
-|-
name | min_component
Command | `-c min_component [R or G or B]`
Input  | an image 
output | `min_component [R or G or B] (x,y): value`

**Usage**
```bash
freud.exe -f ./images/input/image.jpeg -c min_component R
or
freud.exe -f ./images/input/image.jpeg -c min_component G
or
freud.exe -f ./images/input/image.jpeg -c min_component B
```
**Output**
```bash
min_component R (1098, 897): 11
or
min_component G (35, 1337): 0
or
min_component B (1078, 956): 0
```

**Describe tips for implementing feature**
Use the result from the function `read_image_data` from `estia-image.h`, `pixelRGB` struct, and its functions.

