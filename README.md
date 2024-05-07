# EX:09 Implementation-of-Erosion-and-Dilation
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


# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```python
img = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Syed Mokthiyar',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```


# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```


# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![Screenshot 2024-05-06 232432](https://github.com/syedmokthiyar/erosion--dilation/assets/118787294/2b977a40-62f3-422b-9f5b-3690400c967f)



### Display the Eroded Image
![Screenshot 2024-05-06 232516](https://github.com/syedmokthiyar/erosion--dilation/assets/118787294/05b713c0-edfd-48bf-961f-cdf901251472)



### Display the Dilated Image
![Screenshot 2024-05-06 232538](https://github.com/syedmokthiyar/erosion--dilation/assets/118787294/df983e57-c123-4a49-b5d6-fb818f4530a9)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
