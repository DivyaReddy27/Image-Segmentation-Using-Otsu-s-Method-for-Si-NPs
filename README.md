# Image-Segmentation-Using-Otsu-s-Method-for-Si-NPs

## Overview

This project implements an automated image processing pipeline for analyzing silicon nanoparticle (Si-NP) deposition from optical microscopy images. The workflow combines histogram normalization, contrast enhancement, Otsu thresholding, image segmentation, and particle quantification to estimate:

* Particle distribution
* Surface coverage
* Nanoparticle density
* Cluster formation patterns

The implementation is inspired by research on nanoparticle characterization using computer vision techniques and provides a reproducible framework for analyzing microscopy images of spin-coated and drop-casted samples.

---

## Why This Project?

Analyzing nanoparticle deposition manually is time-consuming and often inconsistent. This project automates the process using image processing techniques, enabling rapid and objective evaluation of nanoparticle films.

The pipeline helps researchers compare different deposition methods and process parameters by extracting quantitative metrics directly from microscopy images.

---

## Key Features

### Image Normalization

* Histogram matching against a reference image
* Reduces illumination variations between samples
* Ensures consistent analysis across datasets

### Contrast Enhancement

* Adaptive contrast stretching
* Improves nanoparticle visibility
* Enhances segmentation quality

### Automatic Segmentation

* Otsu's thresholding method
* Separates nanoparticles from the substrate background
* Fully automatic threshold selection

### Particle Analysis

* Surface coverage calculation
* Connected component labeling
* Cluster density estimation
* Nanoparticle count approximation

### Visualization

* RGB histogram comparison
* Cumulative distribution functions (CDF)
* Segmentation results
* Random patch inspection
* Threshold distribution plots

---

## Processing Pipeline

```text
Microscopy Image
        │
        ▼
Histogram Matching
        │
        ▼
Contrast Stretching
        │
        ▼
Grayscale Conversion
        │
        ▼
Otsu Thresholding
        │
        ▼
Binary Segmentation
        │
        ▼
Connected Component Analysis
        │
        ▼
Particle Statistics
```

---

## Technologies Used

* Python
* OpenCV
* NumPy
* Matplotlib
* Scikit-Image

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/nanoparticle-image-analysis.git
cd nanoparticle-image-analysis
```

Install dependencies:

```bash
pip install numpy matplotlib opencv-python pillow scikit-image
```

---

## Dataset

The project was developed using optical microscopy images of silicon nanoparticles deposited through:

* Spin Coating
* Drop Casting

Images are captured under UV illumination where nanoparticles exhibit photoluminescence, making them distinguishable from the silicon substrate.

---

## Methodology

### 1. Histogram Matching

A reference image is selected and used to normalize all target images. This minimizes brightness and illumination differences between experiments.

### 2. Contrast Stretching

Intensity values are rescaled using percentile-based stretching to improve foreground-background separation.

### 3. Otsu Segmentation

The optimal threshold is automatically calculated to separate nanoparticle regions from the substrate.

### 4. Particle Quantification

Connected component labeling identifies nanoparticle clusters and calculates:

* Number of clusters
* Surface coverage percentage
* Estimated particle density

---

## Sample Outputs

### Histogram Matching

* Original Image
* Reference Image
* Matched Image

The histogram distributions become aligned after normalization, reducing imaging bias.

### Segmentation

The segmented output highlights nanoparticle regions while suppressing background pixels.

### Surface Coverage

The percentage of substrate area occupied by nanoparticles is calculated automatically.

### Cluster Density

Connected component analysis estimates nanoparticle cluster distribution across the sample.

---

## Example Results

```text
Distribution of Particles : 12864

Surface Coverage : 27.44%

Estimated Number of Particles :
1.15 × 10^10
```

These metrics can be used to compare deposition quality and nanoparticle distribution across different experimental conditions.

---

## Research Reference

This implementation is based on the methodology presented in:

"Using Otsu's Method for Image Segmentation to Determine the Particle Density, Surface Coverage and Cluster Size Distribution of 3 nm Si Nanoparticles" by Juveiriah M. Ashraf et al. published in IEEE Transactions on Nanotechnology (2021).

## The paper demonstrates how histogram normalization, contrast stretching, Otsu thresholding, and connected component labeling can be combined to analyze nanoparticle deposition quantitatively.

## Future Improvements

* Deep learning-based segmentation
* Cluster size distribution analysis
* Automated batch processing
* Interactive dashboard
* Real-time microscopy integration
* Advanced morphological measurements

---

## Project Goals

The goal of this project is to bridge computer vision and nanotechnology by providing a simple yet effective framework for automated nanoparticle characterization.

By replacing manual measurements with image analysis, researchers can obtain faster, more consistent, and reproducible results.

---

## Author

Developed as a Computer Vision and Image Processing project focused on nanoparticle characterization and microscopy image analysis.

