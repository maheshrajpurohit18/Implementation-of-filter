# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.



## Program:
### Developed By   : MAHESH RAJ PUROHIT J
### Register Number: 212222240058
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("shinchan.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



```

iv) Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()



```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```
## OUTPUT:
### 1. Smoothing Filters


</br>

i) Using Averaging Filter

![Screenshot 2024-03-22 104701](https://github.com/maheshrajpurohit18/Implementation-of-filter/assets/118749665/1fdb5a22-a739-4a12-8299-c8b5845c4113)
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>
![Screenshot 2024-03-22 104746](https://github.com/maheshrajpurohit18/Implementation-of-filter/assets/118749665/0109dda3-864b-4f0e-9b02-b31cb365d920)

</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>
</br>
![Screenshot 2024-03-22 104820](https://github.com/maheshrajpurohit18/Implementation-of-filter/assets/118749665/2baadfd5-6cc0-4519-ae35-ec284d4f9f2e)

</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
![Screenshot 2024-03-22 104859](https://github.com/maheshrajpurohit18/Implementation-of-filter/assets/118749665/584c6f55-cb2b-401f-860a-e43a41f12322)

</br>
</br>
</br>

### 2. Sharpening Filters
</br>


i) Using Laplacian Kernal
</br>
</br>
![Screenshot 2024-03-22 104931](https://github.com/maheshrajpurohit18/Implementation-of-filter/assets/118749665/c3f67e35-f222-44f1-b687-7fa981d1ad85)

</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
![Screenshot 2024-03-22 104959](https://github.com/maheshrajpurohit18/Implementation-of-filter/assets/118749665/e523db4a-3ea2-403d-b2b6-ba6f1b9b48aa)

</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
