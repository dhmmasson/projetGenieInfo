---
title: "Feature #2: Color of the first pixel"
description: "Print the color in RGB of the first pixel (top, left or coordinates 0,0) in the output terminal."
Milestone: 1
Issue: 2
---

## Feature description

Print the color in RGB of the first pixel (top, left or coordinates 0,0) in the output terminal.
A possible prototype: 
```c
void first_pixel (char *source_path);
```

Parameters|value
-|-
name | first_pixel
Command | `-c first_pixel`
Input  | an image 
output | `first_pixel: R, G, B`<br> R, G, B are the integer values of the components in the range 0-255 

## Usage

```bash
freud.exe -f ./images/input/image.jpeg -c first_pixel 
```
## Output

```bash
first_pixel: 89, 139, 164
```
## Describe tips for implementing feature

Define first_pixel in `src/features.h`. Implement first_pixel in `src/features.c`.
Use the `data` from the function `read_image_data` from `<estia-image.h>`.
```c
int read_image_data(const char *filename, unsigned char **data, int *width, int *height, int *channel_count);
```
The components R, G, B of the first pixel are the three first values of  `data`  unsigned char array. 
Read the [wiki](https://github.com/Estia-1a/projetGenieInfo_public/wiki/Image)
Call `first_pixel` in `src/main.c`. See the `helloworld` example to correctly call the function.
```c
if ( strncmp( configuration.command, "first_pixel", 11 ) == 0 ) {
    /* first_pixel() function is defined in feature.h and implemented in feature.c */
    first_pixel();
}
```
