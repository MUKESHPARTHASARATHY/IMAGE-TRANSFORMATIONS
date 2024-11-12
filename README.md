
## EX-4 IMAGE-TRANSFORMATIONS
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4
Display the modified image output.

### Step5:
End the program.



## Program:

## Developed By: MUKESH P

## Register Number: 212222240068

i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()
```
ii) Image Scaling
```import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,50],
              [0,1,50],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 
```
iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```
iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  
```
v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()  
```
vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("cat.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:150 ,10:250]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

![dip4 1](https://github.com/user-attachments/assets/6f0380a1-97d5-4527-84b2-e35fa29f7cae)

### ii) Image Scaling

![dip4 2](https://github.com/user-attachments/assets/ddbf5a73-aa7a-4198-a4a1-b71703b84618)




### iii)Image shearing
![4 3](https://github.com/user-attachments/assets/c102f2bb-b71b-4f8b-af39-9dc82e573897)


![4 4](https://github.com/user-attachments/assets/5bfa1fba-61b1-40c1-9e16-49549be725b5)



### iv)Image Reflection

![4 5](https://github.com/user-attachments/assets/8d183370-e5e0-4f68-962a-fafa2dd7b71c)

![4 6](https://github.com/user-attachments/assets/bc6f23d5-a4dd-43b4-a998-66e38e8bf6ab)






### v)Image Rotation

![4 7](https://github.com/user-attachments/assets/4a2038fd-dcc2-41f2-91ef-50ac41b2afb8)



### vi)Image Cropping

Original
![4 8](https://github.com/user-attachments/assets/f06a2157-f757-476f-8002-efba4d71fd58)

![4 9](https://github.com/user-attachments/assets/8f862a80-387d-489b-9f69-6fbb75d91159)



Cropped

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
