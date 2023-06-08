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
![image](https://github.com/Rohith-AIDS/Opening-and-Closing/assets/94980736/aa418c3c-0a85-4d84-9175-950b1d1abb2a)



### Result of Opening
![image](https://github.com/Rohith-AIDS/Opening-and-Closing/assets/94980736/290cdd6c-1207-4793-91b9-952b7748cbd2)

### Result of Closing
![image](https://github.com/Rohith-AIDS/Opening-and-Closing/assets/94980736/49753d3b-e687-484b-9f9c-060fced5ab9c)


## RESULT:
Thus, the Opening and Closing operation is used in the image using python and OpenCV.
