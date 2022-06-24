### EX NO : 10
### DATE  : 28.05.2022
# <p align="center">Implementation of Erosion and Dilation</p>


## AIM:
To implement Erosion and Dilation using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.

<br/><br/><br/><br/><br/>

## PROGRAM:
```
/*
Developed by   : Graham Stanes
Register Number: 212220230020
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,450),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img1,'Graham',(6,80),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img1)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Erode the image
image_erode1=cv2.erode(img1,kernel)
plt.axis('off')
plt.imshow(image_erode1)
plt.show()

# Dilate the image
image_dilate1=cv2.dilate(img1,kernel)
plt.axis('off')
plt.imshow(image_dilate1)
plt.show()
```

<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>

## OUTPUT:

### Display the input Image
![1](https://user-images.githubusercontent.com/75235488/172896461-10f7fa5c-6b26-42a1-833c-21db05f8db93.png)

### Display the Eroded Image
![2](https://user-images.githubusercontent.com/75235488/172896502-99d853a9-1480-4b54-b57b-f67aea739895.png)

### Display the Dilated Image
![3](https://user-images.githubusercontent.com/75235488/172896540-e1ef435b-b806-4958-8e66-3a02d78ab525.png)

## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.
