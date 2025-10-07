# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages
### Step2:
create the text using cv2.put Text
### Step3:
create the structuting element
### Step4:
Erodde the image
### Step5:
Dilate the image

 
## Program:

``` 
import cv2
import numpy as np
from matplotlib import pyplot as plt
imput_image='actor.jpg'
color_image=cv2.imread(imput_image)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
edges=cv2.Canny(gray_image,100,200)
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
erosion=cv2.erode(edges,kernel,iterations=1)
dilation=cv2.dilate(edges,kernel,iterations=1)
plt.figure(figsize=(15,10))
plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('black and white image')
plt.axis('on')
plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('edge segmentation')
plt.axis('on')
plt.subplot(2,3,4)
plt.imshow(edges,cmap='gray')
plt.title('erosion')
plt.axis('on')
plt.subplot(2,3,5)
plt.imshow(edges,cmap='gray')
plt.title('dilation')
plt.axis('on')

```
## Output:

### Display the input Image

<img width="456" height="505" alt="image" src="https://github.com/user-attachments/assets/d86603c2-d8df-435b-b6ab-f3a8322a88ac" />

### Display the Eroded Image

<img width="590" height="635" alt="image" src="https://github.com/user-attachments/assets/9e674cb6-1690-4c7b-a62d-819262af4c60" />

### Display the Dilated Image

<img width="588" height="622" alt="image" src="https://github.com/user-attachments/assets/833ff7a2-9831-41c5-b4c4-1dd4dd035e5e" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
