# image-debluring-and-upscaling
## Overview
This project focuses on enhancing image clarity by applying deep learning techniques for **image deblurring** and **super-resolution**. It uses **Real-ESRGAN** for high-quality upscaling and sharpening, ensuring visually improved and high-resolution outputs.

## Features
- **Image Deblurring:** Removes motion blur and defocus using deep learning models.
- **Super-Resolution:** Upscales images while maintaining high perceptual quality.
- **Adaptive Sharpening:** Enhances details while preventing over-sharpening.
- **Contrast Enhancement:** Uses CLAHE (Contrast Limited Adaptive Histogram Equalization) for improved visual quality.
- **Batch Processing:** Supports processing multiple images in a folder.

## Dependencies
Ensure you have the following dependencies installed:
```python
pip install torch==1.12.1 torchvision==0.13.1 --extra-index-url https://download.pytorch.org/whl/cu113
pip install opencv-python-headless==4.6.0.66
pip install numpy==1.23.5
pip install pillow==9.4.0
pip install tqdm==4.64.1
pip install basicsr facexlib gfpgan realesrgan
```

## How It Works
### 1. Image Deblurring
The **image_deblurring.py** script processes blurry images, restoring sharpness using deep learning models.

### 2. Super-Resolution
The **super_res.py** script applies **Real-ESRGAN** to upscale images and enhance details, leveraging Residual-in-Residual Dense Blocks (RRDB).

### 3. Adaptive Sharpening
The model uses a sharpening technique based on edge detection to intelligently enhance image clarity.

### 4. Contrast Enhancement
CLAHE is used to enhance contrast while avoiding excessive brightness adjustments.

## Usage
### 1. Run Image Deblurring
```python
python code_image_deblurring.py --input input_folder --output output_folder
```
### 2. Run Super-Resolution
```python
python code_super_res.py --input input_folder --output output_folder --scale 4
```

### 3. Batch Processing
To process an entire folder:
```python
python code_super_res.py --input path_to_images --output enhanced_output --scale 4
```

## Model Used
- **Real-ESRGAN** (Enhanced Super-Resolution GAN) for high-quality upscaling.
- **CNN-based deblurring techniques** to remove motion blur and improve image quality.

## References
1. Sun et al. (2015) - "Learning a Convolutional Neural Network for Non-Uniform Motion Blur Removal."
2. Wang et al. (2018) - "ESRGAN: Enhanced Super-Resolution Generative Adversarial Networks."
3. Xintao Wang et al. (2018) - "Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data."

## Contributing
Feel free to fork this repository and contribute by improving the models or adding new features!
