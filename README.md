# Lab 8 - Frequency Domain Filtering

## Overview
This lab focuses on applying image processing techniques in the frequency domain using Fourier Transform methods.  
The lab demonstrates how filtering operations can be performed using FFT instead of spatial convolution.

---

## Technologies Used
- Python
- NumPy
- Matplotlib
- SciPy
- scikit-image

---

# Frequency Domain Concepts

The lab uses:
- Fourier Transform (FFT)
- Frequency spectrum visualization
- Frequency domain filtering
- Inverse Fourier Transform (IFFT)

---

# Assessment Task - Sobel Filter in the Frequency Domain

The objective of this task is to apply Sobel edge detection filters in the frequency domain instead of the spatial domain.

Two Sobel kernels were used:

## Sobel X Kernel
```python
[[-1, 0, 1],
 [-2, 0, 2],
 [-1, 0, 1]]
```

## Sobel Y Kernel
```python
[[-1, -2, -1],
 [ 0,  0,  0],
 [ 1,  2,  1]]
```

---

## Steps Performed

1. Load and resize the image.
2. Embed Sobel kernels into zero-padded arrays using `center_embed_kernel`.
3. Apply `ifftshift` to align kernels correctly for FFT.
4. Compute the FFT of:
   - The image
   - Sobel kernels
5. Perform filtering in the frequency domain using multiplication.
6. Apply inverse FFT to recover filtered images.
7. Compute edge magnitude using:

```python
np.sqrt(sobel_x_result**2 + sobel_y_result**2)
```

8. Display:
   - Original image
   - Sobel X result
   - Sobel Y result
   - Edge magnitude image

---

## Results
The Sobel filters successfully detected horizontal and vertical edges in the image using frequency domain processing techniques.

---

## Author
Aalya Hussain Almusabeh