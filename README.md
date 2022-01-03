# Image-Blurring-using-various-filters
An analysis of the use of several blurring filters using python and image processing concepts

###Introduction###

*Blurring a picture reduces its sharpness, making it indistinct and hazy in shape or appearance. This is accomplished by smoothing the colour level transition between pixels.
When we blur a picture, we make the colour transition from one side of an image's edge to another more gradual rather than abrupt. The effect is to smooth out sudden variations in
pixel intensity. To achieve this goal, we must perform a convolution operation using a
specialised matrix, known as the kernel, to the image's matrix.
Blurring is an example of a low-pass filter being applied to a picture. A blurring filter is also known as a low pass filter since it allows low frequency to enter and stops high frequency.The term "frequency" refers to the rate at which the pixel value changes. The pixel value changes fast around the edge; because the blurred image must be smooth, these high frequencies should be filtered off.*

To analyse the effect of blurring on an image, we have used different types of smoothing filters. The drawback of smoothing techniques is the blurring of images, and we use this
drawback as a feature to demonstrate our project. The filters used to blur are:
> 1. Mean Filter (Average Filter/Box Filter)
> 2. Median Filter
> 3. Gaussian Filter
> 4. Bilateral Filter
To end our study of the several filters, we take a test image and blur only a section of it as a real-world application.

#### Mean Filter ####
Average (or mean) filtering is a technique for smoothing images by lowering the amount of variation in intensity between neighbouring pixels. This filter works by taking the average of the pixels in the kernel and replacing it with the centre pixel. The kernel's elements are all the same and add up to 1. The kernel must be of an odd size. As a result, the kernel size is 2a+1 x 2b+1.

**Results**
![image](https://user-images.githubusercontent.com/69236709/147954893-ee788007-70b6-4692-8edc-3f8c59ed52ca.png)


#### Median Filter ####
The median filter is a non-linear digital filtering technique that may be used to reduce impulsive or salt-and-pepper noise. Median filtering is commonly employed in digital image processing because it retains edges while reducing noise under specific conditions. It is similar to the mean filter, although it frequently performs a better job of keeping relevant detail in the image than the mean filter. The median filter, like the mean filter, examines each pixel in the picture in turn and compares it to its neighbours to determine whether or not it is typical of its surroundings. It replaces the pixel value with the median of nearby pixel values rather than the mean of those values. The median is derived by first numerically sorting all of the pixel values in the surrounding neighbourhood and then replacing the pixel under consideration with the middle pixel value.

**Results**
![image](https://user-images.githubusercontent.com/69236709/147955010-43113ad1-d804-4a93-8cf5-ab5b01024af9.png)


#### Gaussian Filter ####
The Gaussian smoothing operator is a 2-D convolution operator for blurring pictures and removing detail and noise. It is similar to the mean filter, but it employs a different kernel that depicts the shape of a Gaussian ('bell-shaped') hump. As entries in the kernel, this filter assigns a distinct weight to each element in the matrix. The pixel closest to the selected pixel has a higher weight, while the pixel further away has a lower weight. The Gaussian function returns a weighted average of each pixel's neighbourhood, with the average weighted more toward the value of the central pixels. This is in contrast to the mean filter's uniformly weighted average. As a result, a Gaussian filter provides softer smoothing and greater edge preservation than a similarly sized mean filter. The use of a Gaussian Blur filter prior to edge detection is intended to minimise the amount of noise in the image.

**Results**
![image](https://user-images.githubusercontent.com/69236709/147955094-39bf6514-d2f9-41e2-b716-d5ec23d15680.png)


#### Bilateral Filter ####
A bilateral filter is a non-linear, edge-preserving, and noise-reducing smoothing filter for images. It replaces the intensity of each pixel with a weighted average of intensity values from nearby pixels. This weight can be based on a Gaussian distribution. It can be used in a non-iterative manner. This makes the parameters easy to set since their effect is not cumulative over several iterations.
We can utilize bilateral blurring to minimise noise while retaining edges. By introducing two Gaussian distributions, bilateral blurring achieves this. The first Gaussian function just takes into account spatial neighbours. That is, pixels that seem close together in the image's (x, y)-coordinate space. The second Gaussian then models the neighborhood's pixel intensity, ensuring that only pixels with comparable intensities are included in the blur computation.

**Results**
![image](https://user-images.githubusercontent.com/69236709/147955198-7a2a71d5-048e-456e-ab4f-cc01a742ea59.png)

**blurring only part of an image**
![image](https://user-images.githubusercontent.com/69236709/147955327-a7163a3c-09d8-433a-ab00-570163f3b613.png)


