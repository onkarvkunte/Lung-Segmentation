# Lung-Segmentation

# U-Net Based Lung Segmentation: A Deep Learning Approach

This repository contains the implementation and methodology for a U-Net-based model designed for lung segmentation in medical imaging. The project focuses on enhancing segmentation accuracy with innovative preprocessing, model architecture, and post-processing steps.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Usage](#usage)
- [Contributors](#contributors)
- [License](#license)

## Introduction

Lung segmentation is critical in medical imaging for accurate diagnosis and treatment planning, especially for diseases like lung cancer. This project leverages the U-Net architecture, a powerful encoder-decoder framework, to achieve high-precision segmentation. With the integration of a novel post-processing layer, the model achieves state-of-the-art performance in metrics like Intersection over Union (IoU) and Dice coefficient.

## Features

- **U-Net Architecture**: Designed for medical imaging, featuring robust encoder-decoder blocks.
- **Post-Processing Layer**: Removes minor segmentation inaccuracies for cleaner results.
- **Data Augmentation**: Techniques like resizing, normalization, and random transformations to enhance training robustness.
- **High Accuracy**: Achieved a Dice score of 0.9394 and IoU score of 0.8904.

## Dataset

The dataset consists of chest X-ray images preprocessed to ensure uniformity and quality for training. Data augmentation techniques like brightness adjustment, Gaussian blur, and resizing to 512x512 pixels were applied.

## Model Architecture

### Encoder
- Downsamples features with convolutional layers and max pooling.
- Extracts multiscale features crucial for segmentation.

### Bottleneck
- Processes compressed representations for high-level feature extraction.

### Decoder
- Upsamples and reconstructs spatial information.
- Integrates features from the encoder using skip connections.

### Post-Processing Layer
- Applies thresholding to refine segmentation masks.
- Removes unnecessary components for precise segmentation boundaries.

## Results

- **Without Post-Processing**:
  - Dice Score: 0.9195
  - IoU Score: 0.8536
- **With Post-Processing**:
  - Dice Score: 0.9394
  - IoU Score: 0.8904

These results demonstrate the significant improvement brought by the post-processing layer.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/onkarvkunte/LungSegmentation.git
   cd LungSegmentation
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Train the model:
   ```bash
   python train.py --config config.yaml
   ```

4. Evaluate the model:
   ```bash
   python evaluate.py --model_path checkpoints/model.pth
   ```

## Contributors

- **Onkar Kunte**  
  Lead Developer and Researcher  
  Email: okunte@mail.yu.edu  
  [ResearchGate Profile](https://www.researchgate.net/profile/Onkar-Kunte)

