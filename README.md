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

Create the Text using cv2.putText.
### Step3:

Create the structuring element.

### Step4:
Use Opening operation.
### Step5:

Use Closing Operation.
 
## Program:
# Name: Pavithra S
# Regno: 212223230147

```

# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Pavithra S', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))

# Use Opening operation
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

# Use Closing Operation
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
<img width="511" height="127" alt="Screenshot 2025-11-02 212723" src="https://github.com/user-attachments/assets/f853a8c6-958c-4889-81ce-c651b3ecd905" />


### Display the result of Opening
<img width="525" height="123" alt="Screenshot 2025-11-02 212728" src="https://github.com/user-attachments/assets/6e69cdf1-efe3-428a-a257-fb2ea5c68fd0" />


### Display the result of Closing

<img width="525" height="132" alt="Screenshot 2025-11-02 212734" src="https://github.com/user-attachments/assets/e54d44c0-bb7e-47ea-903c-ac083e2a87df" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
