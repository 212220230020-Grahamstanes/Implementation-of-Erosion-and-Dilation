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

![WhatsApp Image 2022-06-24 at 11 12 15 PM](https://user-images.githubusercontent.com/75235150/175614637-6751c852-c8b0-4b1d-830a-d37278918e78.jpeg)

### Display the Eroded Image
![WhatsApp Image 2022-06-24 at 11 12 15 PM (2)](https://user-images.githubusercontent.com/75235150/175614706-1a78cb68-b977-4a38-b609-5bf2d458a3bf.jpeg)

### Display the Dilated Image
![WhatsApp Image 2022-06-24 at 11 12 15 PM (1)](https://user-images.githubusercontent.com/75235150/175614768-083c93b5-21f2-40d7-a1c5-904a0e6bb57e.jpeg)


## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.
