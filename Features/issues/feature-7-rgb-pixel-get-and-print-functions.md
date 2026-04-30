# Feature #7: RGB pixel, get and print functions

- State: open
- Milestone: Milestone 1: Tutorial
- Labels: export, tutorial
- Assignees: None
- Created: 2022-06-02T12:32:47Z
- Updated: 2023-06-21T08:12:59Z
- URL: https://github.com/Estia-1a/projetGenieInfo_template/issues/7

## Description

**Feature description**
To facilitate access to pixels of the data array, we propose to define a structure and a function to access to specific pixel at position x,y. 


Parameters|value
-|-
name | print_pixel
Command | `-c print_pixel <X> <Y>`
arguments | X: x coordinate of the pixel <br> Y: y coordinate of the pixel
Input  | an image 
output | `print_pixel (x, y): R, G, B` (with R, G, B the component values of pixel at (x,y))

**Usage**
```bash
freud.exe -f ./images/input/image.jpeg -c print_pixel 45 500
```
**Output**
```bash
print_pixel (45, 500): 160, 190, 200
```


First, you have to define a structure for a RGB pixel in `utils.h`. Complete the given struct in `utils.h` with the `pixelRGB` attributes: R, G, and B unsigned char.

Second you have to define the prototype of `get_pixel` function in `utils.h`.
We propose the following prototype for this function: 
```c
pixelRGB * get_pixel( unsigned char* data, const unsigned int width, const unsigned int height, const unsigned int n, const unsigned int x, const unsigned int y );
```

Parameters|value
-|-
data | the data array containing R, G, and B components of each pixels
width | image width
height | image height
n | channel count
x | position x of the pixel we want to return
y | position y of the pixel we want to return

With data the array resulting from the function `read_image_data` from `<estia-image.h>`. Same for width, height, and n.
```c
int read_image_data(const char *filename, unsigned char **data, int *width, int *height, int *channel_count);
```

Then, you have to implement the `get_pixel` function in `utils.c`. 

- The function returns NULL if x or y are beyond range. 
- The function returns NULL if data is NULL
- If these preconditions are verified, then the function returns the address of the requested RGBpixel : 
```c
  return (pixelRGB *) &data[ /* TO COMPLETE */] ;
```

Repeat these steps to define and implement `print_pixel`. This function prints on the command line RGB values of the corresponding pixel.
```c
void print_pixel( char *filename, int x, int y );
```

**Describe tips for implementing feature**
Read the [wiki](https://github.com/Estia-1a/projetGenieInfo_public/wiki/Image) to see the structure of the data array buffer, and also how the [structure](https://github.com/Estia-1a/projetGenieInfo_public/wiki/Image#pixelrgb-structure-end-milestone-1-tutorial) can relate to the array.
