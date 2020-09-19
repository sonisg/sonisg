# Morphological processing
Morphological operations are operations based on image shapes and more generally on binary images. Two images are required for this. The first is an original image and the second is called the kernel or structuring element.
They take the input image and the structuring element and are joined using set operations.
Some of the morphological operations are: Erosion, dilation, opening and closing.

Input Image

![Input Image](https://docs.opencv.org/trunk/j.png)


## Erosion
Erosion is similar to soil erosion. It erodes the boundaries of the foreground image. It diminishes the features of the image.
The kernel slides through the original image. If all the pixel in the kernel image is 1 then only the pixel in the original image be considered as 1 otherwise it will be 0 i.e it will be eroded.
In simple words the thickness of the image decreases or the white region gets reduced.

Erosion

![Erosion](https://docs.opencv.org/trunk/erosion.png)

Useful for removing white noises and detach two connected corners.

## Dilation
It is the opposite of erosion. Here the only 1 pixel in the kernel image is 1 then the pixel is original image can be considered as 1 otherwise 0. So this increase the thickness and the white region.

Dilation

![Dilation](https://docs.opencv.org/trunk/dilation.png)


Useful in joining broken parts of the image.

## Opening
This is erosion followed by dilation.

Opening

![Opening] (data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAHAAAACWCAAAAAAjllMIAAACzklEQVR4nO2b3VLEIAyFi+P7v3K9ci2Qn5PkUGUtV12nk68nDZCE2s7j3vFxM+8BPsANgJ9EW+04DndaN87Eb68rzx7HpU28XAgMDArQU8UGNuPXCuBIsIl7vsP/BrSn/jsoXA6MrcZ8hQ6fDrxjtziVa3GQ9sPvBc23RnPpifF4CtGx4zz840BGmtiOA19vaDs+mtfwXAoS68BIykYBBkcZGBRYBkZ5VWCYVwReeeBE3Cto4g6tATO8rVyaElgA5njknGYlMClwn6DJCswC07wkcObB6W0KmNeXA1Z4GWCJlwDWeHGgzMNLoiiwqC+a6pdxQeCUwiQeIADsrKfrWBjYixl4ATwGHF1XqNOhKCXyAIWFhToDJONsoBj0p3dDAmjYkeVFRAtAncdoIs1RupaHT3xWiwwEirjUUg4BHXUh8S6Q3W2cg6YjnPTupqAQZdxdriXHRucWv1aQBsNqn45wwKNdx/gGhX3HuAz0z376n8tL7vHGalffETg/19oaX7htadBI7dScS1+WLI/KtQjzAx4dd3mwmkt1gWrts6htotdaa1xqlJIZoBcyZinJVzj4e3yoBNAU6ODYCl0cFTjFrviK40BlTqCVaxgo8qQ/KiFcdqkiWF2Dol8qYPuSYXTJ9mSJSPfaUrQAENzi/RcEAdGMCYmHTCeqgMt0ogowF8gIkgDQxaXKcRVo4gqVvwK01VU6DfJKQ+jeh4AOj96gFTvOLNEzkNngRoBmjkd4ghHon4YUFQ9Bwzl9sUavUP8+BirQkKHu+Ks+kuyAF4EDj7cSyEvbKA///w13XBWq74nIE9/h0m9ckTSRKRABUnmhRJji6gsQLotYwFt4IrDJ15zgdRTSeVfgj8VvTOPz+vowfDSaGJ1Ldau8xQebh8TFrgcqhpmL66BwRRZjAiXj3M1jeoejefaRpdQ24W4PAHDp2PGE9AE+wHcDfgFtZXd/UNzSxgAAAABJRU5ErkJggg==)


Used to remove internal noise in an image.

