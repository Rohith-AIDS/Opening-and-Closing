# OPENING-AND-CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.
## PROGRAM:
Developed by : Gunaseelan G

Register number : 212221230031
### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
text_image = np.zeros((100,190),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Guna",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
```
### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

### Use Opening operation
```python
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image,'magma')
plt.axis('off')
```
### Use Closing Operation
```python
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image,'magma')
plt.axis('off')
```

## OUTPUT:

### Input Image
![out1](https://github.com/Guru-Guna/Opening-and-Closing/assets/93427255/e5a91cc0-3082-4ed0-8901-98b3bf779327)


### Result of Opening
![out2](https://github.com/Guru-Guna/Opening-and-Closing/assets/93427255/d44748c0-2042-41ad-b889-df1ea6d79707)

### Result of Closing
![out3](https://github.com/Guru-Guna/Opening-and-Closing/assets/93427255/9fe75b0e-7773-48c1-85c2-82c236a0bfc6)

## RESULT:
Thus, the Opening and Closing operation is used in the image using python and OpenCV.
