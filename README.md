# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save an image as scolor.jpeg

### Step2:
Use imread to read and display the image

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and view the output image windows

## Program:
```
# Developed By: M Parshwanath
# Register Number:212221230073
```
```
# READ AND DISPLAY THE IMAGE
import cv2
scolor=cv2.imread('img3.jpeg')
cv2.imshow('Original Image',scolor)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

```
#Convert BGR and RGB to HSV and GRAY
#BGR2HSV
hsvimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
grayimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2HSV
hsvimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
grayimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
```
#CONVERT HSV TO RGB AND BGR
#HSV TO RGB
rgbimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',rgbimg)
cv2.waitKey(0)
cv2,destroyAllWindows()

#HSV TO BGR
bgrimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgrimg)
cv2.waitKey(0)
cv2,destroyAllWindows()
```
```
# CONVERT RGB AND BGR TO YCrCb
#BGR TO YCrCb
ybgr=cv2.cvtColor(scolor,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',ybgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB TO YCrCb
yrgb=cv2.cvtColor(scolor,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',yrgb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
# SPLIT AND MERGE RGB IMAGE
blue=scolor[:,:,0]
green=scolor[:,:,1]
red=scolor[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()
```
```
# SPLIT AND MERGE HSV IMAGE
hsv = cv2.cvtColor(scolor, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()
```

## Output:
### 1. Original image
![img1](https://user-images.githubusercontent.com/95388047/228000872-96bda938-d09c-4690-848e-9c0f5f039f57.png)

### 2. BGR and RGB to HSV and GRAY
### i) BGR TO HSV
![img2](https://user-images.githubusercontent.com/95388047/228000941-e71be6d5-86c9-4326-9c34-465ee847d20f.png)
### ii) BGR TO GRAY
![img3](https://user-images.githubusercontent.com/95388047/228001410-8bfc49e6-cec6-473b-a3e4-67d8de294253.png)
            
### iii) RGB TO HSV
![img4](https://user-images.githubusercontent.com/95388047/228001620-4755942d-119e-4c6a-bbe4-2de0190738e4.png)

### iV) RGB TO GRAY
![img5](https://user-images.githubusercontent.com/95388047/228001694-07ff0b0d-b812-4eb4-b2f5-46b7e3f8cff6.png)

### 3. HSV to RGB and BGR
### i) HSV TO RGB
![img6](https://user-images.githubusercontent.com/95388047/228001740-851ae924-bd48-4e29-ab51-f13f5f5992ae.png)
### ii) HSV TO BGR
![img7](https://user-images.githubusercontent.com/95388047/228001900-2cb4d6cf-af02-4fc9-826b-6e62e02cfdea.png)


### 4. RGB and BGR to YCrCb
### i) RGB TO YCrCb
![img8](https://user-images.githubusercontent.com/95388047/228002154-f71cc43d-5f5c-43aa-aed4-859074298384.png)

### ii) BGR TO YCrCB
![img9](https://user-images.githubusercontent.com/95388047/228002200-1ecba2de-c0a4-480c-867f-3f657e414588.png)


### 5. Split and merge RGB Image
![img10](https://user-images.githubusercontent.com/95388047/228002352-6e8a59b8-80ed-427a-afa0-0d673da8992f.png)
![img11](https://user-images.githubusercontent.com/95388047/228002413-45d562a6-9f30-4e7b-9f07-2ac344c09efb.png)
![img12](https://user-images.githubusercontent.com/95388047/228003158-9f7e6576-498e-4cc2-930a-e08d7f50c043.png)
![img(13)](https://user-images.githubusercontent.com/95388047/228003189-3254ddee-9c40-46da-9e5f-d47bd8fe62a1.png)

### 6. Split and merge HSV Image
![img13](https://user-images.githubusercontent.com/95388047/228003253-8c56f4ca-1294-4f46-ab5e-74159c7738ed.png)
![img14](https://user-images.githubusercontent.com/95388047/228003287-e643cbaa-8c30-4fe2-be86-7e0a66b940fa.png)
![img15](https://user-images.githubusercontent.com/95388047/228003319-b21defb4-da1a-4a54-b25c-73033c88cbc2.png)
![img16](https://user-images.githubusercontent.com/95388047/228003339-24c1f327-0235-4357-84d3-a5ada075623f.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
