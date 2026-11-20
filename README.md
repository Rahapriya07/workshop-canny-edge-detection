# WORKSHOP 3 – CANNY EDGE DETECTION
## Name: Raha Priya Dharshini M
## Reg No.: 212224240124

## Aim
To detect edges in an image using the Canny Edge Detection technique with OpenCV and Python.

## Software Requirements
- Python
- OpenCV
- Matplotlib
- Jupyter Notebook


## Procedure

1. Import the required libraries, OpenCV and Matplotlib.
2. Read the input image in grayscale using `cv2.imread()`.
3. Apply Gaussian Blur using `cv2.GaussianBlur()` to reduce noise.
4. Apply Canny Edge Detection using `cv2.Canny()` with threshold values 50 and 150.
5. Display the original grayscale image and the detected edges using Matplotlib.
6. Compare the original image with the edge-detected output.

## Code
```

import cv2
import matplotlib.pyplot as plt

# Read the image in grayscale
img = cv2.imread('myfoto.jpg', cv2.IMREAD_GRAYSCALE)

if img is None:
    raise FileNotFoundError("myfoto.jpg not found")

# Apply Gaussian Blur
blurred = cv2.GaussianBlur(img, (5, 5), 0)

# Apply Canny Edge Detection
edges = cv2.Canny(blurred, 50, 150)

# Display Original Image and Detected Edges
plt.figure(figsize=(10, 5))

plt.subplot(121)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(122)
plt.imshow(edges, cmap='gray')
plt.title('Detected Edges')
plt.axis('off')

plt.show()
```

## Output

### Original Image and Detected Edges

<img width="1337" height="542" alt="image" src="https://github.com/user-attachments/assets/ebae258f-2802-426a-9b1e-c98d05c110ba" />


## Result
Thus, Canny Edge Detection was successfully implemented using OpenCV and Python to identify edges in the input image.
