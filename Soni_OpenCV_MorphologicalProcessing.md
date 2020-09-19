# Morphological processing
Morphological operations are operations based on image shapes and more generally on binary images. Two images are required for this. The first is an original image and the second is called the kernel or structuring element.
They take the input image and the structuring element and are joined using set operations.
Some of the morphological operations are: Erosion, dilation, opening and closing.
Input Image
![Input Image](https://docs.opencv.org/trunk/j.png)


## Erosion
Erosion is similar to soil erosion. It erodes the boundaries of the foreground image. It diminishes the features of the image.
The kernel slides through the original image. If the pixel in the kernel image is 1 then only the pixel in the original image be considered as 1 otherwise it will be 0 i.e it will be eroded.
In simple words the thickness of the image decreases or the white region gets reduced.
Erosion
![Erosion](https://docs.opencv.org/trunk/erosion.png)
Useful for removing white noises and detach two connected corners.

## Dilation


