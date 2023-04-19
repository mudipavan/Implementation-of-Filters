# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1
Import the necessary modules.

Step2
Perform smoothing operation on a image.

Step3
Perform sharpening on a image.

Step4
Display all the images with their respective filters.

## Program:
### Developed By   :pavan mudi
### Register Number:212221230067
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
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
![dip p6-1](https://user-images.githubusercontent.com/94828517/233046389-ac8624e6-34b7-48a3-89dc-f535f79672a5.jpg)


ii) Using Weighted Averaging Filter
![dip p6-2](https://user-images.githubusercontent.com/94828517/233046454-f8917018-7cc2-4dd2-b053-ffb19c6e1200.jpg)


iii) Using Gaussian Filter
![dip p6-3](https://user-images.githubusercontent.com/94828517/233046503-fc8190a2-383e-40bb-8649-922a999f43ad.jpg)


iv) Using Median Filter
![dip p6-4](https://user-images.githubusercontent.com/94828517/233046544-76ff6202-1e2e-4343-b69f-065abdda5d50.jpg)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![dip b6-5](https://user-images.githubusercontent.com/94828517/233046601-fa9aa2cb-cec0-4420-a87f-c8e14ecd8f58.jpg)


ii) Using Laplacian Operator
![dip p6-6](https://user-images.githubusercontent.com/94828517/233046674-8efb2039-b01a-4b3e-ac47-88ebde71ad47.jpg)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
