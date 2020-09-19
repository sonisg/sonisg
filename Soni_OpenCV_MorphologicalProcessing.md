# Morphological processing
Morphological operations are operations based on image shapes and more generally on binary images. Two images are required for this. The first is an original image and the second is called the kernel or structuring element.
They take the input image and the structuring element and are joined using set operations.

## Why use morphological processing?
The main function is to remove imperfections in structure of the image.

Some of the morphological operations are: 
1. Erosion
2. Dilation 
3. Opening 
4. Closing

Input Image

![Input Image](https://docs.opencv.org/trunk/j.png)


## Erosion
Erosion is similar to soil erosion. It erodes the boundaries of the foreground image. It diminishes the features of the image.
The kernel slides through the original image. If all the pixel in the kernel image is 1 then only the pixel in the original image be considered as 1 otherwise it will be 0 i.e it will be eroded.
In simple words the thickness of the image decreases or the white region gets reduced.

Syntax -  `cv2.erode(input_image, kernel, iterations) `

Erosion

![Erosion](https://docs.opencv.org/trunk/erosion.png)

**Application**- Used for removing white noises and detach two connected corners.

## Dilation
It is the opposite of erosion. Here the only 1 pixel in the kernel image is 1 then the pixel is original image can be considered as 1 otherwise 0. So this increase the thickness and the white region.

Syntax -  `cv2.dilate(input_image,kernel,iterations)`

Dilation

![Dilation](https://docs.opencv.org/trunk/dilation.png)

**Application**- Used in joining broken parts of the image.

## Opening
This is erosion followed by dilation. Goal of opening is to remove false positives, sometimes you get pixels in the background you can remove that using this method.

Syntax-  `cv2.morphologyEx(input_image, cv2.MORPH_OPEN, kernel)`

Opening

![Opening](http://docs.opencv.org/trunk/opening.png)

**Application**- Used to remove internal noise in an image.

## Closing
It is opposite of opening. Simply dilation followed by erosion. The goal of closing to remove the false negatives. This is where your main image lies and you need to remove the holes from here.

Syntax-  `cv2.morphologyEx(input_image, cv2.MORPH_CLOSE, kernel)`


Closing

![Closing](https://docs.opencv.org/trunk/closing.png)

**Application**- Used to remove small holes inside the foreground image.

