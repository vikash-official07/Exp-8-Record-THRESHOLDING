# Exp-8-Record-THRESHOLDING
# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

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

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** M.MAHENDIRAN

**Register No:** 212225230165

## Output
### ORIGINAL
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("baseball.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```
<img width="872" height="540" alt="image" src="https://github.com/user-attachments/assets/764b793d-d0e4-4e4f-b9df-f2d5c3451e96" />


### Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="891" height="542" alt="image" src="https://github.com/user-attachments/assets/0e6f77c4-6e3a-48bd-8885-b25d1f955758" />

### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="862" height="552" alt="image" src="https://github.com/user-attachments/assets/9542b68c-92ff-4b83-ac99-bab71c483e58" />


### Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
<img width="909" height="536" alt="image" src="https://github.com/user-attachments/assets/17827d38-d9db-4165-9f23-dfa5ba315a16" />

### Otsu's Thresholding
```

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```

<img width="869" height="527" alt="image" src="https://github.com/user-attachments/assets/27d8f9c2-f1bd-4a6b-a96b-f9e9bdf70733" />


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
