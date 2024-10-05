# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step 2:
Translate the image.
### Step 3:
Scale the image.
### Step 4:
Shear the image.
### Step 5:
Reflect of the image.
### Step 6:
Rotate the image.

## Program:
```python
Developed By: Shehan Shajahan
Register Number: 212223240154
```

i) Original Image
```python
# To show the original image and to find the shape of the image
import cv2
import numpy as np
img = cv2.imread('cat.jpg',-1)
original = cv2.cvtColor(img , cv2.COLOR_BGR2RGB)
cv2.imshow('input',original)
cv2.waitKey(0)
cv2.destroyAllWindows()
original.shape
row, col, dim =original.shape
```

ii) Image Translation
```python
translation = np.float32([[1,0,100],[0,1,150],[0,0,1]])
translated_image = cv2.warpPerspective(original,translation,(col,row))
cv2.imshow('translated_image',translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


iii)Image shearing
```python
shear_x = np.float32([[1,0.7,0],[0,1,0],[0,0,1]])
shear_y = np.float32([[1,0,0],[0.3,1,0],[0,0,1]])
sheared_x= cv2.warpPerspective(original,shear_x,(col,row))
sheared_y = cv2.warpPerspective(original,shear_y,(col,row))
cv2.imshow('shear_x',sheared_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('shear_y',sheared_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


iv)Image Reflection
```python
ref_x = np.float32([[1,0,0],[0,-1,row],[0,0,1]])
ref_y = np.float32([[-1,0,col],[0,1,0],[0,0,1]])
reflect_x= cv2.warpPerspective(original,ref_x,(col,row))
reflect_y = cv2.warpPerspective(original,ref_y,(col,row))
cv2.imshow('reflected_x',reflect_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('reflected_y',reflect_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



v)Image Rotation
```python
angle = np.radians(15)
mat_rotate = np.float32([[np.cos(angle),-
(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotate_img =cv2.warpPerspective(original,mat_rotate,(col,row))
cv2.imshow('rotated',rotate_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



vi)Image Cropping
```python
cropped_img=img[10:500,25:600] 
cv2.imshow('after_cropping',cropped_img);
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### i) Original Image
![image](https://github.com/user-attachments/assets/3854750c-7bd6-4802-b736-77d5fd5d30ea)


### ii) Image Translation
![image](https://github.com/user-attachments/assets/d5d36cac-3dfd-457c-9c01-a8c95eb4a189)


### iii)Image shearing
![image](https://github.com/user-attachments/assets/99403f05-501b-4906-89e0-26f09544e85d)
![image](https://github.com/user-attachments/assets/c6cf9fc5-a62b-417a-8b4e-9ee56c69a235)


### iv)Image Reflection
![image](https://github.com/user-attachments/assets/49479d68-3516-4da4-baa9-9060e7b42970)
![image](https://github.com/user-attachments/assets/6f884b99-d1ed-4376-9fb8-ec7b62f6034e)


### v)Image Rotation
![image](https://github.com/user-attachments/assets/e5cdebce-75a7-4a71-858c-40db299b335e)


### vi)Image Cropping
![image](https://github.com/user-attachments/assets/0a35db78-f3a0-4010-94bb-0acb75d88c6d)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
