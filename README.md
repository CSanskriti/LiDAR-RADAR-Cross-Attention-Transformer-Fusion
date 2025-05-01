# Radar-LiDAR Fusion for 3D Object Detection

## Project Overview

This repository contains the implementation of a deep learning model for 3D object detection using Radar-LiDAR sensor fusion. The goal is to develop a robust perception system for autonomous vehicles by combining the high spatial resolution of LiDAR with the weather-resilient properties of radar.

## Features

- Cross-attention-based transformer architecture for dynamic sensor fusion
- Processes 3D point clouds from LiDAR and radar sensors
- Detects objects and regresses 3D bounding boxes (position, size, orientation)
- Visualization tools for attention maps and detection results

## Dataset

The model is trained and evaluated on the NuScenes dataset, which provides synchronized data from:
- 1 × 32-beam LiDAR
- 5 × radar sensors
- 6 × cameras

NuScenes includes 1000 scenes with 3D bounding box annotations across 23 object classes, recorded in diverse environments and weather conditions.

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/[username]/radar-lidar-fusion.git
   cd radar-lidar-fusion
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Set up the NuScenes dataset following the official guidelines.

## Usage

To train the model:
```bash
python train.py --config configs/fusion_config.yaml
```

To evaluate:
```bash
python evaluate.py --checkpoint runs/best_model.pth
```

To visualize attention maps:
```bash
python visualize_attention.py --checkpoint runs/best_model.pth
```

## Results

The model achieves improved mean Average Precision (mAP) and recall over single-sensor baselines. Attention map visualizations confirm effective fusion of radar and LiDAR data, though further enhancement of radar feature utilization is identified as a future goal.

## Future Work

- Improve radar feature representation
- Incorporate camera data into the fusion pipeline
- Explore temporal fusion across multiple frames
- Optimize for deployment on embedded hardware


