# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

## Developed By

## Name: Mukesh B
## Register No: 212223230128
### Original Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("mukesh.jpeg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```
### Erosion
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```
### Dilation
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```
## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.
<img width="403" height="427" alt="image" src="https://github.com/user-attachments/assets/69962cb4-fa8b-4b8a-889f-a953c54035da" />

### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.
<img width="404" height="430" alt="image" src="https://github.com/user-attachments/assets/0839ef92-55e1-48e0-a5cb-7662135c0098" />

### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.
<img width="409" height="431" alt="image" src="https://github.com/user-attachments/assets/59702fa9-10cd-46cb-b9cf-5d35ec464a8a" />

## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
