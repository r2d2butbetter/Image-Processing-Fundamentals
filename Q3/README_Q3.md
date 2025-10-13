## **Image Stitching**
- Implementation of SIFT-based image stitching with RANSAC homography estimation from scratch

### Images Used:
- [uttower_left.JPG](./uttower_left.JPG)
- [uttower_right.JPG](./uttower_right.JPG)

### Image Output (Panorama):
- Stitched panorama image with blended overlapping regions

### Parameter Info:
In `stitch_images` function which creates panorama:
- `img1`: First input image (left)
- `img2`: Second input image (right)

Internally calls:
- `detect_and_compute_sift(img)`: Detects SIFT keypoints and computes descriptors
  - `make_gaussian_pyramid(img, tot_octaves=3, tot_scales=5, sigma=1.6)`
  - `make_dog_pyramid(gaussian_pyramid)`
  - `find_extrema(dog_pyramid, contrast_threshold=0.01)`
  - `assign_orientations(keypoints, gaussian_pyramid)`
  - `extract_descriptors(keypoints, gaussian_pyramid)`
- `match_descriptors(desc1, desc2, ratio_threshold=0.75)`: Matches descriptors using Lowe's ratio test
- `ransac_homography(matches, kp1, kp2, threshold=5.0, max_iterations=2000)`: Estimates homography
- `warp_image(img, H, output_shape)`: Warps image using homography
- `blend_images(warped1, img2, canvas_shape, offset_x, offset_y)`: Blends images with averaging in overlap

stitch_images(img1, img2)