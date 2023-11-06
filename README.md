# IMAGETRANSFORMATION

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

Developed By: Lubindher S

Register Number: 212222240056


### To show the original image
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()
```

### i) Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat2.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,250],
              [0,1,250],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 
```            

### ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat2.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()  
```            

### iii) Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat2.jpeg")
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

### iv) Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat2.jpeg")
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

### v) Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat2.jpeg")
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

### vi) Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("cat2.jpeg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[1000:2500 ,500:2500]
plt.imshow(cropped_img)
plt.show()
```
## Output:

### Original Image
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/2eaab54c-48d5-4e59-80b5-62cd955849ba)

<br>
<br>

### i) Image Translation
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/7307d192-270e-4b9a-a105-aff1300c496c)

<br>
<br>

### ii) Image Scaling
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/36bf1388-e16a-43c6-b52a-f78fd68361b8)

<br>
<br>

### iii) Image shearing
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/a23254c5-cd94-4426-a788-05ea84c9c985)
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/dc4b7839-1db0-49f8-bfd3-adb780d3750c)

<br>
<br>

### iv) Image Reflection
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/97d650d4-2eb4-41e9-86a8-558b3e45c83e)
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/bfcfd4da-bb79-4177-b339-496cece44a15)

<br>
<br>

### v) Image Rotation
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/b61dcad3-19e8-4918-84b5-013d5c31e9d5)
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/9145af2d-ce2e-4449-9aff-5142c38c2e40)

<br>
<br>

### vi) Image Cropping
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/0283bab5-81b6-45a2-840e-3d0309be278f)
![download](https://github.com/aldrinlijo04/IMAGETRANSFORMATION/assets/118544279/6db160cb-dc86-4b63-b669-be85bcffdcbf)

<br>
<br>

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
