# Image-Transformation
## Aim:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the required libraries and read the original image.

### Step 2:
Translate the image.
### Step 3:
Scale the image.

### Step 4:
Shear the image.

### Step 5:
Find reflection of image.
### Step 6:
Rotate the image.
### Step 7:
Crop the image.

### Step 8:
Display all the Transformed images.

## Program:
~~~
Developed By: Gunaseelan G
Register Number:212221230031
~~~
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("car_6.png")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(img)
plt.show()
rows,cols,dim=img.shape
~~~
### i) Image Translation:
~~~
M=np.float32([[1,0,40],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()
~~~
### ii) Image Scaling:
~~~
M=np.float32([[2,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
~~~
### iii) Image shearing:
~~~
M_x=np.float32([[1,0.3,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.2,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
~~~

### iv) Image Reflection:
~~~
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
~~~

### v) Image Rotation:
~~~
angle=np.radians(30)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
~~~
### vi) Image Cropping:
~~~
cropped_img=img[20:190,60:285]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
~~~
## Output:
## Original Image:
![car_6](https://user-images.githubusercontent.com/93427255/231221848-56d408e7-62f6-4326-8642-89357f7a7339.png)



## i) Image Translation:

![5 11](https://user-images.githubusercontent.com/93427255/231221185-97095cea-21d9-428d-af3e-d5922bfdd1f0.png)



## ii) Image Scaling:

![5 12](https://user-images.githubusercontent.com/93427255/231221938-c5c326b9-4819-4b81-9763-c4414f33c898.png)




## iii) Image shearing:

![5 13](https://user-images.githubusercontent.com/93427255/231222001-87e6bfd4-8b6a-4ccc-9434-932d508cfdfd.png)




## iv) Image Reflection:

![5 14](https://user-images.githubusercontent.com/93427255/231222062-2cbb9399-34f0-404b-ba9d-a8f6d6279e28.png)



## v) Image Rotation:

![5 15](https://user-images.githubusercontent.com/93427255/231221360-de9bfa00-7464-4473-9fa8-dc00339e6a7f.png)



## vi) Image Cropping:


![5 16](https://user-images.githubusercontent.com/93427255/231222104-64ce3dae-b8a4-4e7f-89bc-8453e29cdf92.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
