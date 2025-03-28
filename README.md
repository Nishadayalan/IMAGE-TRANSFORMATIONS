# IMAGE-TRANSFORMATIONS


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

### Step4:
Display the modified image output.

### Step5:
End the program.



## Program:
```python
# Developed By: NISHA D
# Register Number: 212223230143
```
# i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('christ.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)  

# 1. Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]]) 
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))

# 2. Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR) 

# 3. Shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]]) 
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))

# 4. Reflection (Flip)
reflected_image = cv2.flip(image_rgb, 1) 
# 5. Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1) 
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))

# 6. Cropping
cropped_image = image_rgb[50:300, 100:400]  

# Plot the original and transformed images
plt.figure(figsize=(12, 8))

plt.subplot(2, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')

plt.subplot(2, 3, 2)
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')

plt.subplot(2, 3, 3)
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')

plt.subplot(2, 3, 4)
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')

plt.subplot(2, 3, 5)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')

plt.subplot(2, 3, 6)
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')

plt.tight_layout()
plt.show()

# Plot cropped image separately as its aspect ratio may be different
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()

```
## Output:
```python
# Developed By: NISHA D
# Register Number: 212223230143
```

![image](https://github.com/user-attachments/assets/b7376c70-6cac-45c5-be2f-8e41a79d1dc2)


![image](https://github.com/user-attachments/assets/6f18cc83-a5ae-42a9-b85d-1f2f83a26680)

![image](https://github.com/user-attachments/assets/3ab17098-0d1b-4062-a683-a1b3207328eb)

![image](https://github.com/user-attachments/assets/420afac4-4880-4f72-91e1-16c20ed3ef40)

![image](https://github.com/user-attachments/assets/a1158ce5-a88f-4a1f-9b7f-76ff6ee292a3)


![image](https://github.com/user-attachments/assets/29829688-c83b-4c33-a8b4-b59734849252)


![image](https://github.com/user-attachments/assets/f43d5602-0469-474c-a55c-f8f9e65f61c8)







## Result: 


Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
