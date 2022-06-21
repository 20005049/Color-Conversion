## EXP NO:03
## DATE:
## Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.
## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
 Convert BGR and RGB to HSV and GRAY
### Step2:
Convert HSV TO RGB AND BGR
### Step3:
Convert RGB and BGR to YCrCb
### Step4:
To Split and merge RGB Image
### Step5:
To Split and merge HSV Image
## Program:
```python
# Developed By: Sri Harish M
# Register Number: 212220230047
# i) Convert BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('jk.jpg')
cv2.imshow('Original Image',img)
img1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',img1)
img2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',img2)
img3 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',img3)
img4 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',img4)
cv2.waitKey(0)
# ii)Convert HSV to RGB and BGR
cv2.imshow('Original Image',img)
img5 = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',img5)
img6 = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',img6)
cv2.waitKey(0)
# iii)Convert RGB and BGR to YCrCb
cv2.imshow('Original Image',img)
img7 = cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',img7)
img8 = cv2.cvtColor(img,cv2.COLOR_BGR2YCrCb)
cv2.imshow('RCB2YCrCb',img8)
cv2.waitKey(0)
# iv)Split and Merge RGB Image
red = img[:,:,0]
green = img[:,:,1]
blue = img[:,:,2]
img9=cv2.merge((blue,green,red))
cv2.imshow('Merged',img9)
cv2.waitKey(0)
# v) Split and merge HSV Image
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow("ORIGINAL HSV_IMAGE",hsv)
h,s,v = cv2.split(hsv)
img10=cv2.merge((h,s,v))
cv2.imshow('Merged',img10)
cv2.waitKey(0)
```
## Output:
### i) BGR and RGB to HSV and GRAY
![e1](https://user-images.githubusercontent.com/75241366/162791568-486f49b5-b86e-42f1-ab0f-8393e1231086.jpg)
### ii) HSV to RGB and BGR
![e2](https://user-images.githubusercontent.com/75241366/162791588-af1df659-0b48-476a-b980-2423ccee06a3.jpg)
### iii) RGB and BGR to YCrCb
![e3](https://user-images.githubusercontent.com/75241366/162791603-5d59e6bb-0ec4-4b26-8fc1-fffc618507e6.jpg)
### iv) Split and merge RGB Image
![e4](https://user-images.githubusercontent.com/75241366/162791609-30027f00-72e8-4e83-9dec-e42cbbf0c737.jpg)
### v) Split and merge HSV Image
![e5](https://user-images.githubusercontent.com/75241366/162791623-3987380a-8230-47fc-8a75-f8fd80916027.jpg)
## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
