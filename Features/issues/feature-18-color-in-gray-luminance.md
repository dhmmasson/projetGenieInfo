# Feature #18: Color in gray (luminance)

- State: open
- Milestone: Milestone 3: Colors
- Labels: export, colors
- Assignees: None
- Created: 2022-06-02T14:38:53Z
- Updated: 2022-06-08T09:59:11Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/18

## Description

**Feature description**
Transform the image to keep only a gray version, but with a smarter computation than a simple average of the R, G, B components.
The resulting image with a simple average will lake luminosity.
Instead, try to use the [luminosity formulae](https://en.wikipedia.org/wiki/Grayscale#Colorimetric_(perceptual_luminance-preserving)_conversion_to_grayscale) with the given values **0.21, 0.72, and 0.07** like in the pseudo-code below:

```c
unsigned char value = 0.21 * getPixel(x, y)->R + 0.72 * getPixel(x, y)->G + 0.07 * getPixel(x, y)->B
```


Parameters|value
-|-
name         | color_gray_luminance
Command | `-c color_gray_luminance`
Input          | an image 
output       | a new image `image_out.bmp` that keeps only a gray version of the input image

**Usage**
```bash
./freud.exe -f images/input/image.jpeg -c color_gray_luminance
```
**Output**
A new image `image_out.bmp` as a gray version of the input image



**Tips for implementing the feature**
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
|<img src="https://user-images.githubusercontent.com/14878561/171637527-c63fb289-c5a0-43d2-a04f-fe75ff7a51dd.jpeg" width="250px">|<img src="https://user-images.githubusercontent.com/14878561/171641480-351368ee-6c63-4587-9459-5283e59c93e2.jpg" width="250px">|

 
