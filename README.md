# Adaptive Color Ratio Based Segmentation (ACRS)

## 📌 Overview
This repository presents an Adaptive Color Ratio Based Segmentation (ACRS) algorithm for detecting and extracting Acute Promyelocytic Leukemia (APML) blast cells from microscopic blood smear images.

## 🔬 Key Contribution
The proposed method introduces an adaptive threshold defined as:

T = max(G/B) / max(R/B)

This allows dynamic adaptation to variations in staining and illumination.

## ⚙️ Methodology

### 1. Ratio Computation
- G2B = G / B
- R2B = R / B

### 2. Adaptive Threshold
- T = max(G2B) / max(R2B)

### 3. Segmentation Rule
A pixel is classified as blast cell if:
- R ≤ B
- (G/B) ≤ T
- Pixel is not white

### 4. Post-processing
- Median filtering (noise removal)
- Morphological operations
- Watershed segmentation (cell separation)

### 5. Cell Extraction
- Each segmented cell is cropped
- Padded to fixed size (150×150)
- No distortion (aspect ratio preserved)

## 🚀 Run in Google Colab
Upload image and run all cells in `acrs_colab.ipynb`

## 📦 Output
- Binary segmentation mask
- Watershed-separated cells
- Cropped individual cell images

## 📊 Applications
- Leukemia detection
- Medical image preprocessing
- CNN dataset preparation

## 👤 Author
Leow Bin Toh
