# Feature #17: Invert colors

- State: open
- Milestone: Milestone 3: Colors
- Labels: export, colors
- Assignees: None
- Created: 2022-06-02T14:18:59Z
- Updated: 2022-06-08T09:54:31Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/17

## Description

**Feature description**
Transform the image so that colors are inverted (e.g., `new_R = 255 - old_R`).

Parameters|value
-|-
name         | invert
Command | `-c color_invert`
Input          | an image 
output       | A new image `image_out.bmp` with inverted colors compared to the input image

**Usage**
```bash
./freud.exe -f images/input/image.jpeg -c color_invert
```
**Output**
A new image `image_out.bmp` with inverted colors compared to the input image


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
|<img src="https://user-images.githubusercontent.com/14878561/172585237-5831263d-aad5-474a-9fd5-50d271931cc0.jpeg" width="250px"> |<img src="https://user-images.githubusercontent.com/14878561/172585578-ed32ff51-df9d-4a37-9d00-c7b2048959f8.jpg" width="250px">|



 
