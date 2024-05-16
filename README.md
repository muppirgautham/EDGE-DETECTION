# EDGE-DETECTION
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

### program:
```
Developed by: M Gautham
Register No: 212221230027
```

# Import the packages
```
import cv2
import matplotlib.pyplot as plt
```

# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("cycle.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

# SOBEL EDGE DETECTOR

## SOBEL X AXIS:
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
## SOBEL Y AXIS:
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBEL XY AXIS:
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

# LAPLACIAN EDGE DETECTOR
```

lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

# CANNY EDGE DETECTOR
```

canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()


```

## Output:
### SOBEL EDGE DETECTOR

### SOBEL X AXIS:
![image](https://github.com/muppirgautham/EDGE-DETECTION/assets/94810884/b60954bb-df6a-421f-9a1f-67ed78f6418c)

### SOBEL Y AXIS:
![image](https://github.com/muppirgautham/EDGE-DETECTION/assets/94810884/2aa61596-e40f-4c41-b7a5-a20c778e1ef3)

### SOBEL XY AXIS:
![image](https://github.com/muppirgautham/EDGE-DETECTION/assets/94810884/a24ecd8a-67cc-4f33-a16b-c077959516cf)

### LAPLACIAN EDGE DETECTOR:
![image](https://github.com/muppirgautham/EDGE-DETECTION/assets/94810884/26e530f8-42ad-4939-8939-a3414cb7784d)

### CANNY EDGE DETECTOR:
![image](https://github.com/muppirgautham/EDGE-DETECTION/assets/94810884/d617461f-e2c3-45cb-bd29-c92b7eb322cc)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
