# CervixAttenNet: Transformer-Based MR-to-CT Synthesis for Radiotherapy Planning

## Overview

This repository contains the implementation of **CervixAttenNet**, a transformer-based deep learning model for synthetic CT (sCT) generation from MR images. This work is part of our study submitted to Scientific Reports. The method aims to improve the accuracy of MR-only radiotherapy planning for cervical cancer by generating high-quality sCT images.

The repository will be made publicly accessible upon the acceptance of the manuscript for publication.

## Features

- Transformer-based architecture with query-selected attention for improved image synthesis.
- Comprehensive evaluation using image quality metrics (e.g., MAE, PSNR, SSIM) and dosimetric analysis.
- Code for data preprocessing, model training, and evaluation.

## Repository Contents

- `src/`: Main code for the model implementation.
- `data/`: Scripts for data preprocessing and augmentation.
- `results/`: Example outputs, including sCT images and evaluation metrics.
- `README.md`: Overview and usage instructions.

## Requirements

- Python 3.8+
- PyTorch 1.10+
- CUDA 11.0+
- Additional dependencies are listed in `requirements.txt`.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/JianJuly/CervixAttenNet.git
   cd CervixAttenNet
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### 1. Preprocess Data
Use the scripts in the `data/` directory to prepare your MRI and CT datasets. Ensure the datasets are formatted as described in the manuscript.

### 2. Train the Model
Run the training script with default settings:
   ```bash
   python src/train.py --config configs/default.yaml
   ```

### 3. Evaluate the Model
Evaluate the trained model on the testing dataset:
   ```bash
   python src/evaluate.py --model checkpoints/best_model.pth
   ```

## Citation

If you use this code, please cite our work:
```
@article{Transformer-Based Magnetic Resonance-to-Computed Tomography Synthesis for Radiotherapy for Cervical Cancer: Model Development and Clinical Evaluation,
  title={Transformer-Based Magnetic Resonance-to-Computed Tomography Synthesis for Radiotherapy Planning},
  author={Jian et al.},
  journal={Scientific Reports},
  year={2025}
}
```

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
