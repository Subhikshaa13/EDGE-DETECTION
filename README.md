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
### PROGRAM:
```
# Import the packages
import cv2

# Load the image, Convert to grayscale and remove noise
i=cv2.imread('land.jpeg',-1)
gray=cv2.cvtColor(i,cv2.COLOR_BGR2GRAY)
img = cv2.GaussianBlur(gray,(3,3),0)


# SOBEL EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
sobel_x=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
cv2.imshow('sobel_x',sobel_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_y=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
cv2.imshow('sobel_y',sobel_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_xy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
cv2.imshow('sobel_xy',sobel_xy)
cv2.waitKey(0)
cv2.destroyAllWindows()


# LAPLACIAN EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
rgb_image = cv2.cvtColor(i,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(rgb_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()


# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(img, 120, 150)
cv2.imshow('canny',canny_edges)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### SOBEL EDGE DETECTOR
![image](https://github.com/Subhikshaa13/EDGE-DETECTION/assets/118787344/db3f108c-f61a-4f67-a436-18f90b50d193)

![image](https://github.com/Subhikshaa13/EDGE-DETECTION/assets/118787344/44d7017f-ed11-4654-b671-6a072cc84dad)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/Subhikshaa13/EDGE-DETECTION/assets/118787344/44d7017f-ed11-4654-b671-6a072cc84dad)
![image](https://github.com/Subhikshaa13/EDGE-DETECTION/assets/118787344/a6d3ac44-9588-4479-8189-e7bb7675be9a)


### CANNY EDGE DETECTOR
![image](https://github.com/Subhikshaa13/EDGE-DETECTION/assets/118787344/b8d36506-ca9d-4f32-b285-c2ffb390720c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
