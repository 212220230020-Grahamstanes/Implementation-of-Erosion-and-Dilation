# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:

Import the necessary packages.

### Step2:

Create the text image using cv2.putText.

### Step3:

Then create the structuring image for dilation/erosion

### Step4:

Apply erosion and dilation using cv2.erode and cv2.dilate

### Step5:

Plot the images using plt.imshow

 
## Program:

``` Python

# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
cv2.putText(img1,'Graham',(5,70),font,2,(255),5,cv2.LINE_AA)


# Create the structuring element

kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
plt.imshow(img1)
plt.axis('off')
plt.title('orginal')

# Erode the image

image_erode=cv2.erode(img1,kernel)
plt.imshow(image_erode)
plt.axis('off')
plt.title('Erosion')

# Dilate the image

image_dilate=cv2.dilate(img1,kernel)
plt.imshow(image_dilate)
plt.axis('off')
plt.title('Dilation')


```
## Output:

### Display the input Image

![output1](https://user-images.githubusercontent.com/75235150/172800657-8dd397bc-22da-4aab-8eae-04edc71ddd20.png)


### Display the Eroded Image
![output2](https://user-images.githubusercontent.com/75235150/172800691-4ba2ce6d-7c45-4d59-936d-baa81d00f868.png)


### Display the Dilated Image
![output3](https://user-images.githubusercontent.com/75235150/172800721-7c01a2f1-da00-4fc0-b5c3-e99045b499ec.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
