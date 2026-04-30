# Feature #13: Color in red

- State: open
- Milestone: Milestone 3: Colors
- Labels: export, colors
- Assignees: None
- Created: 2022-06-02T13:23:28Z
- Updated: 2022-06-08T09:55:35Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/13

## Description

**Feature description**
Transform the image to keep only the red component.

Parameters|value
-|-
name         | color_red
Command | `-c color_red`
Input          | an image 
output       | a new image `image_out.bmp` that keeps only the red component of the input image

**Usage**
```bash
./freud.exe -f images/input/image.jpeg -c color_red
```
**Output**
A new image `image_out.bmp` that keeps only the red component of the input image

**Describe tips for implementing feature**
Use write_image_data from <estia-image.h> to create new image with the new values.

```c
/**
 * Writes into an image file
 * @param[in] filename Name of the file to be written into
 * @param[in] data Reference to the pixel array to be written
 * @param[in] width Width of the image
 * @param[in] height Height of the image
 * @return 0 on failure and non-0 on success.
 */
int write_image_data(const char *filename, unsigned char *data, int width, int height);
```

**Additional information**
Example:
|Input|Output|
|---|---|
|<img src="https://user-images.githubusercontent.com/14878561/171637527-c63fb289-c5a0-43d2-a04f-fe75ff7a51dd.jpeg" width="250px">| <img src="https://user-images.githubusercontent.com/14878561/171638015-1af42836-b37d-477b-94b2-f0396900e98b.jpg" width="250px">|

 
