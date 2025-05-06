# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import required libraries (OpenCV, NumPy) and load the image in grayscale.

### Step2:

Define a structuring element (kernel) for morphological operations.

### Step3:

Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:

Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:

Display and compare the original, eroded, and dilated images.
 
## Program:

``` 
import cv2
import numpy as np
from matplotlib import pyplot as plt
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

cv2.putText(img1,'ARUNMOZHI VARMAN' ,(10,70),font,2,(255),2,cv2.LINE_AA)

kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

plt.figure(figsize=(11, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')

```
## Output:
![Screenshot 2025-05-06 131647](https://github.com/user-attachments/assets/56580134-94e8-4b6e-8470-7f5526735e13)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
