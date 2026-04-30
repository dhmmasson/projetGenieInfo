# Feature #20: Rotate anti-clockwise 90°

- State: open
- Milestone: Milestone 4: Transform
- Labels: export, transform
- Assignees: None
- Created: 2022-06-02T14:45:07Z
- Updated: 2022-06-22T09:07:51Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/20

## Description

**Feature description**
Transform the image with a rotation effect: 90° anti-clockwise rotation.

Parameters|value
-|-
name         | rotate_acw
Command | `-c rotate_acw`
Input          | an image 
output       | a new image `image_out.bmp` that is a 90° anti-clockwise rotation of the input image

**Usage**
```bash
./freud.exe -f images/input/image.jpeg -c rotate_acw 
```
**Output**
A new image `image_out.bmp` that is a 90° anti-clockwise rotation of the input image


