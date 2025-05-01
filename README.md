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



