# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages

### Step 2:
Read the image

### Step 3:
Create the structuring element

### Step 4:
Use Opening operation

### Step 5:
Use Closing Operation

### Step 6:
Display all the output images

## Program:

# Import the necessary packages
```py
import cv2
import matplotlib.pyplot as plt
import numpy as np
```

# Create the Text using cv2.putText
```py
def plot(img):
    plt.imshow(img)
    plt.axis('off')

image = np.zeros((200,1150),dtype='uint8')
font=cv2.FONT_HERSHEY_SCRIPT_COMPLEX
cv2.putText(image,'Meenakshi',(20,140),font,5,(255),3,cv2.LINE_AA)
plot(image)
```

# Create the structuring element
```py
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
```
# Use Opening operation
```py
img1=cv2.morphologyEx(image,cv2.MORPH_OPEN,kernel)
plot(img1)
```
# Use Closing Operation
```py
img2 = cv2.morphologyEx(image,cv2.MORPH_CLOSE,kernel)
plot(img2)
```
## Output:

### Display the input Image
![ss1](./ss1.png)

### Display the result of Opening
![ss2](./ss2.png)

### Display the result of Closing
![ss3](./ss3.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
