# Feature #14: Color in green

- State: open
- Milestone: Milestone 3: Colors
- Labels: export, colors
- Assignees: None
- Created: 2022-06-02T13:26:02Z
- Updated: 2022-06-08T09:56:17Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/14

## Description

**Feature description**
Transform the image to keep only the green component.

Parameters|value
-|-
name         | color_green
Command | `-c color_green`
Input          | an image 
output       | a new image `image_out.bmp` that keeps only the green component of the input image

**Usage**
```bash
./freud.exe -f images/input/image.jpeg -c color_green
```
**Output**
A new image `image_out.bmp` that keeps only the green component of the input image

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
|<img src="https://user-images.githubusercontent.com/14878561/171637527-c63fb289-c5a0-43d2-a04f-fe75ff7a51dd.jpeg" width="250px">|<img src="https://user-images.githubusercontent.com/14878561/171639573-30c6b5ae-8857-42e7-b382-b93299d3f157.jpg" width="250px">|

 
