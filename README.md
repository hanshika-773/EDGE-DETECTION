# **EXPERIMENT NO. 6: EDGE DETECTION**
# **NAME : HANSHIKA VARTHINI R**
# **REG NO : 212223240046**
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### ORIGINAL IMAGE
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('krishh.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### SOBEL EDGE DETECTOR

<img width="398" height="513" alt="image" src="https://github.com/user-attachments/assets/483193f9-ed29-481c-8c3e-6c086a1b8121" />


### LAPLACIAN EDGE DETECTOR

<img width="436" height="500" alt="image" src="https://github.com/user-attachments/assets/6cf723fe-5a0d-4c99-a44b-a464febaabf9" />


### CANNY EDGE DETECTOR

<img width="398" height="507" alt="image" src="https://github.com/user-attachments/assets/f53fc39b-82ed-48be-b1b3-b4bd369b70ea" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
