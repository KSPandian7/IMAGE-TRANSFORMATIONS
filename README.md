# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>

### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
```python
Developed By: KULASEKARAPANDIAN K
Register Number: 212222240052
```

## i)Image Translation
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bc.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[1,0,114],[0,1,-230],[0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

## ii) Image Scaling
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bc.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[2.4,0 ,0],[0,1.9,0],[0,0,1]])
scaled_image = cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```



## iii)Image shearing
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bc.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0.8 ,0],[0,1,0],[0,0,1]])
M_y = np.float32([[1,0,0],[0.6,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.imshow(sheared_img_yaxis)
plt.show()
```



## iv)Image Reflection
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bc.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0 ,0],[0,-1,rows],[0,0,1]])
M_y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.imshow(reflected_img_yaxis)
plt.show()
```



## v)Image Rotation
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bc.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
angle = np.radians(19)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```



## vi)Image Cropping
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bc.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
cropped_img = image[120:800,20:400]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```





## Output:
### Input Image:
![OUTPUT](/bc.jpg)

### i)Image Translation
![OUTPUT](/r1.png)
<br>
<br>
<br>
<br>

### ii) Image Scaling
![OUTPUT](/re2.png)
<br>
<br>
<br>
<br>


### iii)Image shearing
![OUTPUT](/re3.png)
<br>
<br>
<br>
<br>


### iv)Image Reflection
![OUTPUT](/re4.png)
<br>
<br>
<br>
<br>



### v)Image Rotation
![OUTPUT](/re5.png)
<br>
<br>
<br>
<br>



### vi)Image Cropping
![OUTPUT](/re6.png)
<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
