# Thermal Object Detection and Tracking Using Deep Learning

## Overview

This project focuses on developing a robust thermal object detection and tracking system using deep learning techniques. It explores object detection in thermal infrared images, particularly under challenging lighting and visibility conditions.

The project investigates different YOLO architectures and Self-Supervised Learning (SSL) approaches to improve object detection performance while reducing dependency on manually labeled data.

## Objectives

- Develop an object detection system for thermal infrared images.
- Compare different YOLO architectures.
- Explore Self-Supervised Learning for thermal image representation learning.
- Evaluate detection performance with limited labeled training data.
- Implement multi-object tracking for thermal video sequences.

## Dataset

**FLIR Thermal Dataset (YOLOv8 Format)**

Dataset: `naveengumaste/flir-2024-dataset-yolov8-version`

Object classes:
- Car
- Person
- Dog

### Dataset Preprocessing

| Split | Images |
|---|---:|
| Training | 18,035 |
| Validation | 3,865 |
| Testing | 3,865 |
| **Total** | **25,765** |

Data preprocessing included:
- Duplicate image detection using MD5 hashing.
- Removal of duplicate images.
- Dataset restructuring.
- Train, validation, and test split preparation.

## Methodology

### 1. YOLO-Based Object Detection

Three YOLO architectures were evaluated:

- YOLOv10
- YOLOv12
- YOLOv26

### 2. Self-Supervised Learning

The project explores four Self-Supervised Learning approaches:

- SimCLR
- BYOL
- I-JEPA
- DINOv3

The objective is to learn meaningful thermal image representations and investigate their effectiveness when fine-tuning with only 20% labeled data.

### 3. Object Tracking

ByteTrack is used for multi-object tracking in thermal video sequences, enabling object detection and tracking across consecutive frames.

## Experimental Results

### YOLO Model Comparison

| Model | mAP50-95 |
|---|---:|
| YOLOv10 | 0.5255 |
| YOLOv12 | **0.5506** |
| YOLOv26 | 0.5437 |

**Best Performing Model:** YOLOv12

YOLOv12 achieved the highest mAP50-95 score of 0.5506 among the evaluated architectures.

## Technologies Used

- **Programming Language:** Python
- **Deep Learning:** PyTorch
- **Object Detection:** YOLOv10, YOLOv12, YOLOv26
- **Self-Supervised Learning:** SimCLR, BYOL, I-JEPA, DINOv3
- **Object Tracking:** ByteTrack
- **Dataset:** FLIR Thermal Dataset
- **Environment:** Kaggle Notebooks
- **Hardware:** NVIDIA Tesla T4 GPU

## Key Contributions

- Evaluated multiple YOLO architectures for thermal object detection.
- Investigated SSL approaches for thermal image representation learning.
- Explored low-label fine-tuning using 20% labeled data.
- Applied duplicate detection and dataset cleaning techniques.
- Integrated object tracking for thermal video analysis.

## Future Improvements

- Improve detection accuracy under challenging thermal conditions.
- Further evaluate SSL-based feature representations.
- Optimize models for real-time thermal object detection.
- Improve tracking performance in crowded environments.
- Explore deployment on edge devices.

## Author

**Ayon Adhikary**

Computer Science and Engineering

GitHub: [@theayon7](https://github.com/theayon7)

---

*This project explores deep learning, thermal computer vision, self-supervised learning, and multi-object tracking.*
