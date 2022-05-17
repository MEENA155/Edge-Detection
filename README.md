# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.


### Step2:
For performing edge detection on a image.

Sobel
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)
Laplacian
lap=cv2.Laplacian(gray,cv2.CV_64F)
Canny
canny=cv2.Canny(gray,120,150)

### Step3:
Display all the images with their respective edge detected images.



 
## Program:
/*
Developed by: S.Meena.
Registration Number : 212221240028
*/
``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("flowers.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)


# SOBEL EDGE DETECTOR
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



# LAPLACIAN EDGE DETECTOR
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


# CANNY EDGE DETECTOR
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

![Screenshot (61)](https://user-images.githubusercontent.com/94677128/168846781-2df0a03f-fb10-4efe-a64c-e71a6afe0044.png)


![Screenshot (62)](https://user-images.githubusercontent.com/94677128/168846936-c9758cd3-9582-4a28-b0c7-e566988fc526.png)


![Screenshot (63)](https://user-images.githubusercontent.com/94677128/168847043-8372780b-8bbe-4660-8e01-d2db87ab3068.png)





### LAPLACIAN EDGE DETECTOR
![Screenshot (64)](https://user-images.githubusercontent.com/94677128/168847196-509a1dfb-95f9-4864-87f9-5861be8ebddb.png)


### CANNY EDGE DETECTOR
![Screenshot (65)](https://user-images.githubusercontent.com/94677128/168847327-2913375a-2e1a-435a-acdf-3d9f3143487b.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
