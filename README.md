# Histogram of images
## Aim
### To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
### Anaconda - Python 3.7

## Algorithm:
### Step1:
#### Read the gray and color image using imread()

### Step2:
#### Print the image using imshow().

### Step3:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
#### The Histogram of gray scale image and color image is shown.


## Program:

### Colour and Gray Image

```py
# Developed By: Sri Varshan P
# Register Number: 212222240104

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("Gray_Mustang.jpg")
color_image = cv2.imread("Mustang.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### Histogram of Grayscale Image

```py
import numpy as np
import cv2
Gray_image = cv2.imread("Gray_Mustang.jpg")
Color_image = cv2.imread("Mustang.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```

### Histogram of Green channel of colour Image

```py
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```



```py

import cv2
gray_image = cv2.imread("Mustang.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:

### Input Grayscale Image and Color Image

![image](https://github.com/PSriVarshan/Histogram-of-an-images/assets/114944059/3639d338-50c7-404e-9033-83ecfdd1aa74)


### Histogram of Grayscale Image

![image](https://github.com/PSriVarshan/Histogram-of-an-images/assets/114944059/c547a9b0-debc-423a-ae6c-1509d2b59da9) ![image](https://github.com/PSriVarshan/Histogram-of-an-images/assets/114944059/d06d97fa-dfca-4112-9c13-1fca78873694)

### Histogram of Green Channel of colour Image

![image](https://github.com/PSriVarshan/Histogram-of-an-images/assets/114944059/d0450f4b-8d34-4af7-a9fc-0698ddf9cd6b) ![image](https://github.com/PSriVarshan/Histogram-of-an-images/assets/114944059/05db2634-eed9-4ffb-a2a6-ea573ed2fd17)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/PSriVarshan/Histogram-of-an-images/assets/114944059/1a056fe0-32d5-488b-9224-3b42e6ac1727)



## Result: 
### Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
