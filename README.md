# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
```
### Step 1: Import the necessary libraries and read the original image and save it as a image variable.

### Step 2: Translate the image.

### Step 3: Scale the image.

### Step 4: Shear the image.

### Step 5: Reflect of image.

### Step 6:Rotate the image.




### Step 7: Crop the image.

### Step 8: Display all the Transformed images.
```

## Program:
```
Developed By:RAKSHITHA DEVI J
Register Number:212221230082
```
```
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
input_img=cv2.imread("d1.jpeg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
```
i)Image Translation
```
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()
```


ii) Image Scaling
```
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```





iii)Image shearing
```
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```



iv)Image Reflection
```
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```




v)Image Rotation
```
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
ngle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```




vi)Image Cropping
```
import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()



```
## Output:


![image](https://user-images.githubusercontent.com/94165326/230329822-95c26190-3b2b-45b8-b00f-9d2585327926.png)

### i)Image Translation

![image](https://user-images.githubusercontent.com/94165326/230329911-c513fd88-dc9b-4bc3-8fe8-8a164d7bcbb2.png)




### ii) Image Scaling

![image](https://user-images.githubusercontent.com/94165326/230329997-889c20c3-208f-4f47-93f6-cf97b85a30b3.png)


### iii)Image shearing

![image](https://user-images.githubusercontent.com/94165326/230330143-a2fd74d8-88cb-424a-89e1-4ef661affb86.png)


### iv)Image Reflection

![image](https://user-images.githubusercontent.com/94165326/230330245-a65940b8-b703-4567-b27b-2fea6ef3b804.png)


### v)Image Rotation

![image](https://user-images.githubusercontent.com/94165326/230330578-95a2ad7f-fd06-4262-a690-5e7c50640151.png)


### vi)Image Cropping
![image](https://user-images.githubusercontent.com/94165326/230330577-deb56677-23cc-4f46-a323-01786a3008a8.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
