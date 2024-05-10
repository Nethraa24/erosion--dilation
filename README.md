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
Erode the Image

### Step5:
Dilate the Image

 
## Program:

### DEVELOPED BY : J NETHRAA
### REGISTER NO: 212222100031

# Import the necessary packages
```PY
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```PY
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Good',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```PY
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
# Erode the image
```PY
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```PY
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/Nethraa24/erosion--dilation/assets/121215786/8d5f3b0e-fe62-4b90-876d-d6c14a93c6b7)

### Display the Eroded Image
![image](https://github.com/Nethraa24/erosion--dilation/assets/121215786/698f022e-c5be-444e-8b00-af793da17ba5)


### Display the Dilated Image
![image](https://github.com/Nethraa24/erosion--dilation/assets/121215786/9f5db037-f927-40f2-b1ca-9a0d222eb58a)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
