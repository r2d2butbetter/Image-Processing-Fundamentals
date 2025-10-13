## **Corner Detection**
- Implementation of Harris Corner Detection algorithm from scratch

### Images Used:
- [img1.png](./img1.png)
- [img2.png](./img2.png)

### Image Output (Corners Detected):
- Corners are detected and displayed on the input images

### Parameter Info:
In `harris_corner_detector` function which detects corners:
- `img`: Input grayscale image
- `k`: Cornerness constant (sensitivity control)
- `ksize`: Kernel size for Gaussian blur
- `sigma`: Sigma value for Gaussian blur
- `method`: 0 for Det-Trace, 1 for Eigenvalue
- `window_size`: Window size for non-maximum suppression
- `threshold_ratio`: Fraction of max corner response for filtering

harris_corner_detector(img1_input, k=0.01, method=0, window_size=3, threshold_ratio=0.005)
harris_corner_detector(img2_input, k=0.04, method=1, window_size=7, threshold_ratio=0.15)
