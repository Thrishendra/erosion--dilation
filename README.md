# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
## Developed by: T Thrishendra
## Register number: 212223230227
## PROGRAM
```

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'Thrishendra' ,(5,70),font,4,(255),2,cv2.LINE_AA)


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
![WhatsApp Image 2025-05-21 at 15 27 42_0c39b197](https://github.com/user-attachments/assets/400c979f-c9ab-4de3-84b6-8243dc5b56f8)



### Display the Eroded Image
![WhatsApp Image 2025-05-21 at 15 28 39_17b4009c](https://github.com/user-attachments/assets/8b9e6ef8-0861-4314-b15f-83d578ed1839)



### Display the Dilated Image
![WhatsApp Image 2025-05-21 at 15 28 49_2ffd90ef](https://github.com/user-attachments/assets/708edb12-f4d5-4191-b44f-07b383a96bba)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
