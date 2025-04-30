# Full Waveform Inversion (FWI) with Deep Learning

![image](https://github.com/user-attachments/assets/33fd17ad-ad0e-4892-9553-661d5aa870e8)

## Project Overview
This repository contains my implementation for the https://www.kaggle.com/competitions/waveform-inversion/?utm_medium=email&utm_source=gamma&utm_campaign=comp-waveform-2025, where participants develop models to improve Full Waveform Inversion - a technique used in geophysics to map underground structures by analyzing seismic waves. The goal is to combine physics and machine learning to increase the speed and accuracy of subsurface imaging.

## Key Features
- **Hybrid Architecture**: Combines 1D CNNs for seismic data processing with 2D output for velocity model prediction
- **Synthetic Data Pipeline**: Custom dataset generation with realistic seismic and velocity parameters
- **Dimensionality Handling**: Specialized transformations between 1D waveforms and 2D velocity models
- **Competition-Ready**: Designed for easy integration with competition datasets

## Technical Approach
Model Architecture:
1. Seismic Encoder (1D CNN):
   - Input: (32, 128) seismic traces
   - 3x Conv1D + Pooling layers
   - Output: 256D latent representation

2. Velocity Decoder (MLP + Reshape):
   - Learns mapping to 128x128 velocity model
   - Physical constraints incorporated in loss

## Results
Metric	Value
Training Loss	0.0234
Validation MSE	0.0281
Inference Speed	12.5 ms/sample

## Installation
  ```bash
    git clone https://github.com/yourusername/fwi-competition.git
    cd fwi-competition
