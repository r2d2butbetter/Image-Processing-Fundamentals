## **Image Filtering and Hybrid Images**
- Implementation of basic image filtering operations from scratch

### Images Used:
- [image_hybrid_1](./image_hybrid_1.png)
- [image_hybrid_2](./image_hybrid_2.png)

### Image Output (Hybrid Img):
- [hybrid_img.png](./output/hybrid_img.png)

### Parameter Info:
In `create_hybrid_image` function which generates the hybrid img:
- `img_low`: Image for low pass filtering
- `img_high`: Img for high pass filtering
- `k_size_low`: Kernel Size for low pass
- `k_size_high`: Kernel Sixe for Hihg pass
- `sigma_low`: sigma value for low pass
- `sigma_high`: sigma value for high pass
- `alpha`: multiplier to high pass img
- `pad`: padding needed(ALWAYS TRUE)

create_hybrid_image(img1, img2, 5, 7, 15, 1, 10)