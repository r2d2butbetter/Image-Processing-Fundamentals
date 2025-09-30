# Computer Vision Fundamentals - Programming Assignment

This repository contains a comprehensive implementation of fundamental computer vision algorithms and techniques, built from scratch using Python, NumPy, and OpenCV. The project covers core image processing operations, filtering techniques, edge detection, corner detection, and advanced image stitching.

## Repository Structure

### **Notebooks and Implementations**

#### **Q1: Image Filtering and Hybrid Images**
- **File**: `S20230010225Q_1.ipynb`
- **Description**: Implementation of basic image filtering operations from scratch
- **Key Functions**:
  - `cross_correlation_2d()` - 2D cross-correlation operation
  - `convolve_2d()` - 2D convolution using cross-correlation
  - `gaussian_blur_kernel_2d()` - Gaussian kernel generation
  - `low_pass()` - Low-pass filtering for smooth image content
  - `high_pass()` - High-pass filtering for edge preservation
- **Output**: Creates hybrid images by combining low-pass and high-pass filtered versions of different images

#### **Q2: Edge Detection**
- **File**: `S20230010225Q_2.ipynb`
- **Description**: Custom edge detection implementation using Sobel operators
- **Key Features**:
  - Gaussian smoothing for noise reduction
  - Sobel filters for gradient computation
  - Non-maximum suppression for edge thinning
  - Gradient magnitude and orientation calculation
- **Images Used**: `uttower_left.JPG`, `uttower_right.JPG`

#### **Q3: Image Stitching (Custom SIFT Implementation)**
- **File**: `S20230010225Q_3.ipynb`
- **Description**: Complete SIFT (Scale-Invariant Feature Transform) implementation from scratch for panorama creation
- **Key Components**:
  - **Scale-Space Construction**: Gaussian pyramids and DoG pyramids
  - **Keypoint Detection**: Extrema detection with edge suppression
  - **Orientation Assignment**: Dominant orientation calculation
  - **Descriptor Extraction**: 128-dimensional SIFT descriptors
  - **Feature Matching**: Lowe's ratio test for robust matching
  - **RANSAC**: Robust homography estimation
  - **Image Warping**: Bilinear interpolation for perspective transformation
  - **Image Blending**: Seamless panorama creation
- **Output**: Panoramic images from multiple views

#### **Q3: Image Stitching (Alternative Implementation)**
- **File**: `S20230010224Q_3.ipynb`
- **Description**: Earlier version of SIFT implementation with detailed explanations
- **Purpose**: Benchmarking against custom implementation

#### **Q4: Corner Detection**
- **File**: `S20230010225Q_4.ipynb`
- **Description**: Harris corner detection algorithm implementation
- **Key Features**:
  - Hessian matrix computation
  - Cornerness measure calculation: `Det(H) - k*Tr(H)`
  - Alternative implementation using eigenvalues: `λ₁λ₂ - k(λ₁+λ₂)`
  - Performance comparison between methods
- **Images Used**: `img1.png`, `img2.png`

#### **Legacy Implementation**
- **File**: `S20230010225Q_3_inbult.ipynb`
- **Description**: Image stitching using OpenCV's built-in SIFT implementation for comparison

### **Input Images**
- `uttower_left.JPG` - Left view of university tower for panorama stitching
- `uttower_right.JPG` - Right view of university tower for panorama stitching  
- `img1.png` - Test image for corner detection
- `img2.png` - Test image for corner detection
- `image_hybrid_1.png` - Input for hybrid image creation
- `image_hybrid_2.png` - Input for hybrid image creation

### **Output Directory**
- `output/hybrid_img.png` - Generated hybrid image result

### **Documentation**
- [`Programming_Assignment_CV.pdf`](Programming_Assignment_CV.pdf) - Original assignment specifications and requirements

## Key Features

### **From-Scratch Implementations**
- **No built-in filtering functions** - All convolution and correlation operations implemented manually
- **Custom SIFT algorithm** - Complete implementation including scale-space construction, keypoint detection, and descriptor extraction
- **Manual edge detection** - Sobel operators and non-maximum suppression from scratch
- **Custom homography estimation** - Direct Linear Transform (DLT) with SVD solving

### **Advanced Techniques**
- **Multi-scale image analysis** using Gaussian pyramids
- **Robust feature matching** with Lowe's ratio test
- **RANSAC algorithm** for outlier rejection
- **Perspective transformation** with bilinear interpolation
- **Image blending** for seamless panorama creation

### **Computer Vision Concepts Covered**
- Linear filtering and convolution
- Frequency domain analysis (low-pass/high-pass filtering)
- Feature detection and description
- Geometric transformations
- Robust estimation techniques
- Image registration and stitching

## Technical Implementation

### **Core Libraries Used**
- `NumPy` - Numerical computations and array operations
- `OpenCV` - Image I/O and some comparison implementations
- `Matplotlib` - Visualization and plotting
- `SciPy` - Gaussian window generation

### **Key Algorithms**
- **SIFT Pipeline**: Scale-space → DoG → Extrema → Orientation → Descriptors
- **Harris Corner Detection**: Structure tensor → Cornerness measure → Non-maximum suppression
- **RANSAC**: Random sampling → Model fitting → Inlier counting → Best model selection

## Results and Performance

The implementations successfully demonstrate:
- **Hybrid image creation** with adjustable frequency cutoffs
- **Robust edge detection** with noise suppression
- **Accurate corner detection** with sub-pixel precision
- **High-quality panorama stitching** with natural blending
- **Feature matching** with high precision using custom SIFT implementation

## Educational Value

This repository serves as a comprehensive learning resource for:
- Understanding fundamental computer vision algorithms
- Implementing complex mathematical operations from scratch
- Learning best practices in image processing
- Exploring the relationship between theory and practical implementation

## Usage

Each notebook is self-contained and can be run independently. Ensure all required images are in the same directory as the notebooks.

