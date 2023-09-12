# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
Write a code to translation of the image.

### Step3:
Write a code for scaling of the image.

### Step4:
Write a code for shearing of the image.

### Step5:
Write a code for reflection of the image.

### Step6:
Display all the Transformed images.

## Program:

Developed By:PERARASU M    
Register Number: 212222100033

i)Image Translation
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("ben.jpg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
~~~

ii) Image Scaling
~~~
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv
image = cv2.imread("ben.png")
rows,cols,dim = image.shape

M_scale = np.float32([[1,0,0], [0,1.5,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.axis("off")
plt.imshow(scale_image)
plt.show()
~~~

iii)Image shearing
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("ben.png")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
~~~

iv)Image Reflection
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("ben.png")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
~~~


v)Image Rotation
~~~
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("ben.png")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
~~~

vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("ben.png")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

![image](https://github.com/PERARASU10/IMAGETRANSFORMATION/assets/118348589/641da3e6-ffc3-4ab1-a535-e2d3e270b627)


### ii) Image Scaling

![image](https://github.com/PERARASU10/IMAGETRANSFORMATION/assets/118348589/7b24be71-b738-4bfb-8e9b-7693652bc91f)


### iii)Image shearing

![image](https://github.com/PERARASU10/IMAGETRANSFORMATION/assets/118348589/f3b4bba9-148f-4ea1-9142-e982c0c5f2f3)


### iv)Image Reflection

![image](https://github.com/PERARASU10/IMAGETRANSFORMATION/assets/118348589/82ebadea-9e46-4bb2-8851-bc6cff1d26e9)


### v)Image Rotation

![image](https://github.com/PERARASU10/IMAGETRANSFORMATION/assets/118348589/c303e134-769d-4c55-80f3-0552ea8d09aa)


### vi)Image Cropping

![image](https://github.com/PERARASU10/IMAGETRANSFORMATION/assets/118348589/cd102cff-58d3-4f14-93a4-dacbab15faee)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
