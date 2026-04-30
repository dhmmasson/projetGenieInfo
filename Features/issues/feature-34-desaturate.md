# Feature #34: Desaturate

- State: open
- Milestone: Milestone 3: Colors
- Labels: export, colors
- Assignees: None
- Created: 2022-06-08T09:53:08Z
- Updated: 2022-06-08T10:07:21Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/34

## Description

**Feature description**
Transform the image to desaturate colors.

Parameters|value
-|-
name         | color_desaturate
Command | `-c color_desaturate`
Input          | an image 
output       | a new image `image_out.bmp` with desaturated colors from the input image

**Usage**
```bash
./freud.exe -f images/input/image.jpeg -c color_desaturate
```
**Output**
A new image `image_out.bmp`  with desaturated colors from the input image


**Tips for implementing the feature**
Use the formulae of this pseudo-code:
```c
new_val = (min(R, G, B) + max(R, G, B)) / 2;
```



**Additional information**
Example:
|Input | Output|
|---|---|
<img src="https://user-images.githubusercontent.com/14878561/171637527-c63fb289-c5a0-43d2-a04f-fe75ff7a51dd.jpeg" width="250px">|<img src="https://user-images.githubusercontent.com/14878561/172590722-a431daaa-3a85-4937-8504-3896d0626db8.jpg" width="250px">

