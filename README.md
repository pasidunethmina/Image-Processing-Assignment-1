# Image Processing Assignment

This repository contains code and documentation for an image processing assignment that includes:

1. **Histogram Equalization on Foreground Only**  
2. **Sobel Filtering using Separable Kernels**  
3. **Image Segmentation and Background Enhancement using GrabCut**  
4. **Image Zooming with Nearest Neighbor and Bilinear Interpolation**  

---

## Assignment Tasks

### 1. Histogram Equalization on Foreground
- Split the image into Hue, Saturation, and Value channels.
- Use the saturation channel to extract the foreground mask via thresholding.
- Apply histogram equalization **only** to the foreground pixels.
- Combine the enhanced foreground with the background.
- Display the HSV channels, mask, original image, and result.

### 2. Sobel Filtering
- Implement Sobel filtering using the separable property of Sobel kernels:
  
  \[
  \begin{bmatrix} 1 & 0 & -1 \\ 2 & 0 & -2 \\ 1 & 0 & -1 \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \\ 1 \end{bmatrix} * \begin{bmatrix} 1 & 0 & -1 \end{bmatrix}
  \]

- Compute horizontal (Sobel X) and vertical (Sobel Y) edge maps.
- Visualize the results separately without combining them into gradient magnitude.

### 3. GrabCut Segmentation and Background Blur
- Use OpenCV's GrabCut algorithm to segment a flower image into foreground and background.
- Display the segmentation mask, isolated foreground, and background images.
- Create an enhanced image by blurring the background and keeping the flower sharp.
- Explain why the background near the flower edges appears dark.
- Suggestions to improve segmentation (manual mask refinement, larger rectangle).

### 4. Image Zooming and SSD Computation
- Implement image zooming with nearest neighbor and bilinear interpolation (custom and OpenCV versions).
- Test zooming by scaling small images up by a factor of 4.
- Compute the normalized sum of squared differences (SSD) between zoomed images and originals.
- Compare performance and accuracy of interpolation methods.

---

## Requirements

- Python 3.x
- OpenCV
- NumPy
- Matplotlib
