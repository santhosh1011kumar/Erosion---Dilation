# Implementation-of-Erosion-and-Dilation

## NAME : SANTHOSH KUMAR A
## REG NO : 212224230250
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import necessary libraries, including OpenCV (cv2) and Matplotlib (plt), to load, manipulate, and display images.

### Step 2:
Use cv2.putText() to add text to the image at a specific location with chosen font, size, color, and thickness.

### Step 3:
Define a structuring element using cv2.getStructuringElement() to specify the shape and size for morphological transformations.

### Step 4:
Apply erosion to the image using cv2.erode() with the structuring element to shrink white regions and reduce noise.

### Step 5:
Dilate the eroded image using cv2.dilate() with the structuring element to expand white regions and enhance features.

### Step 6:
Display the original and processed images using plt.imshow() with proper axis configuration and titles for comparison.

### Step 7:
Finalize by calling plt.show() to display all images in a single figure for easy visualization and comparison.
 
## Program:


# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create a blank image 
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

# Create the Text using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```


# Create the structuring element
```
print("SANTHOSH KUMAR A")
print("212224230250")
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

```
# Create a simple square kernel
```
kernel = np.ones((3, 3), np.uint8)
```

# Applying Erosion (Shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)

```

# Erode the image
```
print("SANTHOSH KUMAR A")
print("212224230250")
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

```
# Applying Dilation (Expanding effect)
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```

# Dilate the image
```
print("SANTHOSH KUMAR A")
print("212224230250")

plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```
## Output:

### Display the input Image

<img width="760" height="626" alt="image" src="https://github.com/user-attachments/assets/81fc9904-d436-40a6-aedd-d2fd5604b50c" />


### Display the Eroded Image
<img width="729" height="631" alt="image" src="https://github.com/user-attachments/assets/b6d01f31-3ebb-4dec-8849-fba01699378e" />


### Display the Dilated Image
<img width="742" height="614" alt="image" src="https://github.com/user-attachments/assets/c7a5cdb4-57ea-4fb7-ac32-767fe91a62e9" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
