# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Give the input text using cv2.putText().

### Step3:
Perform opening operation and display the result.

### Step4:
Similarly, perform closing operation and display the result.

 
## Program:
```
 Developed by : SUBISHESH P
 REG.NO       : 212223230220
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the text using cv2.putText
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'SUBISHESH', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")

# Use Closing Operation
image2=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2024-10-26 212002](https://github.com/user-attachments/assets/c2548535-77b6-41c4-9cb8-18d979344f16)

### Display the result of Opening
![Screenshot 2024-10-26 212045](https://github.com/user-attachments/assets/c18031a3-c29d-4d21-b59b-1dceb21e02bf)

### Display the result of Closing
![Screenshot 2024-10-26 212053](https://github.com/user-attachments/assets/bbfd26e2-3a30-4a92-9559-7bfae19048c7)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
