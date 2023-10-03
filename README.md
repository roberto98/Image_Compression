# Haar Wavelet Image Compression

📚 "Digital Signal Image Processing" project (Artificial Intelligence, UniGe)

## Overview

This project implements image compression with the Haar wavelet transform. It compares the compression performance against Fourier transform methods. Experiments show that the Haar wavelets outperform Fourier especially on images without much periodicity. The wavelet transform concentrates more energy in fewer coefficients, allowing for effective thresholding and compression. The analysis looks at compression rate versus MSE across grayscale and color images.


## Haar Wavelet Overview

The Haar wavelet is one of the simplest wavelet transforms, developed by Alfréd Haar in 1909. 

The key idea is to decompose the image into low and high frequency components by averaging and differencing. For an image, the 2D Haar wavelet transform is applied by:

1. Taking pairwise averages and differences of image rows 
2. Repeating this on the columns

This results in 4 subbands:

- LL: Low-low frequencies (averaging) 
- LH: Low-high frequencies (horizontal details)
- HL: High-low frequencies (vertical details)  
- HH: High-high frequencies (diagonal details)

The process can be repeated recursively on the LL subband. 

![image](https://github.com/roberto98/Image_Compression/assets/32781888/7c6f8fc5-d813-4807-8599-e7bbf26f2547)

This multi-resolution decomposition concentrates most of the image energy in fewer coefficients. The HH, HL, and LH bands mostly contain small values that can be discarded to achieve compression.

The main advantages of using Haar wavelets for this application are:

- Simple and fast to compute
- Sparse representation of images
- Allows progressive transmission
- Thresholding provides good compression


## ⚙ How to Run
To run the project, follow these steps:

1. Download the .ipynb file from the provided link.
2. Install the required libraries by running the following commands in your terminal or command prompt:
  ```
  pip install numpy
  pip install matplotlib
  pip install scikit-learn
  pip install pywavelets
  ```
3. Open the .ipynb file using Jupyter Notebook or any other compatible IDE.
4. Run the cells in the notebook sequentially, following the instructions and comments provided in the notebook.
