# EX-6 EDGE-DETECTION
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
## PROGRAM:

## DEVELOPED BY: JANANI.V.S
## REGISTER NUMBER: 212222230050

## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("1269810.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![1269810](https://github.com/Mathiofficial/EDGE-DETECTION/assets/118787327/85d1f6b4-5599-4c1b-822a-7b198cd07364)

### SOBEL EDGE DETECTOR:
![Screenshot 2024-04-02 112536](https://github.com/Mathiofficial/EDGE-DETECTION/assets/118787327/6cc6df38-6e5a-40a5-80fa-6764c669bea6)
![Screenshot 2024-04-02 112607](https://github.com/Mathiofficial/EDGE-DETECTION/assets/118787327/434388fb-f9c2-44b3-8138-0e8e6ea4d18b)
![Screenshot 2024-04-02 112638](https://github.com/Mathiofficial/EDGE-DETECTION/assets/118787327/ff2eda91-732d-48a2-957b-4d60b3b46422)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-04-02 112725](https://github.com/Mathiofficial/EDGE-DETECTION/assets/118787327/298d8e19-a0e8-4afe-93b9-acb12c922f1b)
### CANNY EDGE DETECTOR
![Screenshot 2024-04-02 112815](https://github.com/Mathiofficial/EDGE-DETECTION/assets/118787327/4bc8adad-a5c9-41b5-ae49-34b07a3231e3)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
