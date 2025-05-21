# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.
 
## Program:

``` Python
# Developed By: ARSHITHA MS
# Register No: 212223240015


import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,700),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'ANU RADHA N' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')


```
## Output:

### Display the input Image
![WhatsApp Image 2025-05-21 at 15 06 52_54a728c9](https://github.com/user-attachments/assets/0b1ecbac-bcba-40aa-8be2-1ebcdd3efdc3)



### Display the Eroded Image
![WhatsApp Image 2025-05-21 at 15 06 52_effd0c3f](https://github.com/user-attachments/assets/c5ee0b90-61df-495f-a09a-e0f33591afd2)


### Display the Dilated Image

![WhatsApp Image 2025-05-21 at 15 06 53_bcd72970](https://github.com/user-attachments/assets/5019a0be-50d1-4a60-b5dd-5d412155d0e4)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
