## **Edge Detection**
- Implementation of edge detection with gradient computation and non-maximum suppression from scratch

### Images Used:
- [uttower_left.JPG](./uttower_left.JPG)
- [uttower_right.JPG](./uttower_right.JPG)

### Image Output (Edge Detection):
- Edge magnitude images with thinned edges after non-maximum suppression

### Parameter Info:
In `edge_filter` function which detects edges:
- `img0`: Input grayscale image
- `sigma`: Standard deviation for Gaussian smoothing kernel

Internally calls:
- `gaussian_kernel(size, sigma)`: Creates Gaussian kernel with size = 2*ceil(3*sigma)+1
- `convolve_2d(img, kernel, pad=True)`: Convolves image with kernel
- Sobel filters for x and y gradients
- Non-maximum suppression with quantized gradient orientations (0°, 45°, 90°, 135°)

edge_filter(img, sigma=2)