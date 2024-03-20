# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By:Vasanthamukilan M
# Register Number:212222230167
```
### Input Grayscale Image and Color Image
```python
import matplotlib.pyplot as plt
import numpy as np
import cv2
Gray_image = cv2.imread("sea.png")
Color_image = cv2.imread("lake2.jpg")
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```
### Histogram of Grayscale Image and any channel of Color Image
```python
plt.imshow(Gray_image)
plt.show()
hist =cv2.calcHist([Gray_image], [0], None, [256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem (hist)
plt.show()
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image], [1], None, [256], [0,256])
plt.figure()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem (hist1)
plt.show()
```
### Histogram Equalization of Grayscale Image.
```python
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image], [1], None, [256], [0,256])
plt.figure()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem (hist1)
plt.show()
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/Vasanthamukilan/Histogram-of-an-images/assets/119559694/fcd5c36e-3514-4198-87b6-eba36c3bfe99)
![image](https://github.com/Vasanthamukilan/Histogram-of-an-images/assets/119559694/5dfa72f1-444a-4bec-b311-c6f94cb54310)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/Vasanthamukilan/Histogram-of-an-images/assets/119559694/4321cf98-ea6b-4dcf-b0b1-daf73c0cde2f)
![image](https://github.com/Vasanthamukilan/Histogram-of-an-images/assets/119559694/dc0e5e19-3881-480a-a193-11b7db9add00)
![image](https://github.com/Vasanthamukilan/Histogram-of-an-images/assets/119559694/4e202226-1cb6-4d65-bf1d-e1022d78d54b)
![image](https://github.com/Vasanthamukilan/Histogram-of-an-images/assets/119559694/a2c23d16-651b-42c4-a554-194e4ee136f0)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-21 001117](https://github.com/Vasanthamukilan/Histogram-of-an-images/assets/119559694/d2352e96-bc29-4242-aa1f-e35817cfd6d1)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
