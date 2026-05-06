# Milestone 3: Colors

Those features will manipulate pixel data to create a new image with modified colors. You will practice reading pixel data from an image using the estia-image library, manipulating it in C, and writing output to a new image file. These features are very similar to each other, you should implement them in parallel so that everyone gets to practice each of the steps (reading, manipulating, writing). You can still together for the first feature then split the remaining 6 features between you. Read the [collaboration strategies](../../Resources/Collaboration.qmd) to find how to properly split the work and collaborate effectively.

Once the feature are implemented, you could refactor the code to avoid repetition between the different features. You can create a helper function that takes as parameter a pointer to a function that manipulates the pixel data in a specific way. This way you can reuse the same code to read and write the image for all the features, and only change the manipulation of the pixel data. But remember to first implement a code that works before making a better code. 

## Issues
- [#11](../issues/issue-11-color-in-red.md) Color in red 
- [#12](../issues/issue-12-color-in-green.md) Color in green 
- [#13](../issues/issue-13-color-in-blue.md) Color in blue 
- [#14](../issues/issue-14-color-in-gray-grayscale.md) Color in gray (grayscale) 
- [#15](../issues/issue-15-invert-colors.md) Invert colors 
- [#16](../issues/issue-16-color-in-gray-luminance.md) Color in gray (luminance) 
- [#25](../issues/issue-25-desaturate.md) Desaturate 
