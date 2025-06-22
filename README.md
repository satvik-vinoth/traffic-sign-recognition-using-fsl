# traffic-sign-recognition-using-fsl

This repository contains the implementation of various deep learning models for **Traffic Sign Recognition** using **Few-Shot Learning (FSL)**. The models are trained and evaluated using the **Prototypical Network** approach on the **German Traffic Sign Recognition Benchmark (GTSRB)** dataset, with additional testing on Indian traffic signs.

## 🚘 Overview

Autonomous vehicles require accurate traffic sign recognition for safe navigation. Traditional deep learning models struggle with:

- Recognizing new or rare signs
- Real-world challenges like lighting, occlusion, and regional variations
- Need for large labeled datasets and retraining

This project addresses these limitations using **Few-Shot Learning (FSL)** with **Prototypical Networks**, which can classify unseen traffic signs based on only a few labeled examples.

## 🧠 Models Implemented

Each model serves as the **feature extractor** in the Prototypical Network framework:

- `Traffic_Sign_Detection_FSL_CNN_MODEL.ipynb` – Baseline CNN
- `Traffic_Sign_Detection_FSL_CONVIT_MODEL.ipynb` – ConViT-Tiny (Vision Transformer)
- `Traffic_Sign_Detection_FSL_EFFICIENTVIT_B2_MODEL.ipynb` – EfficientViT v2 (Hybrid CNN-ViT)
- `Traffic_Sign_Detection_FSL_MOBILENETV3_MODEL.ipynb` – MobileNetV3 (Lightweight CNN)
- `Traffic_Sign_Detection_FSL_RESNET_MODEL.ipynb` – ResNet18 (Deep CNN)

## 📊 Dataset

- **German Traffic Sign Recognition Benchmark (GTSRB)**  
  - 43 classes  
  - 39,209 training images  
  - 12,630 testing images  
- Preprocessing: Resizing, normalization, and episodic sampling for N-way K-shot tasks

## 🧪 Methodology

- **Few-Shot Learning (FSL)** via **Prototypical Networks**
- **Episodic Training:** N-way, K-shot setup
- **Distance-based Classification:** Euclidean distance from class prototypes
- **Testing Strategy:** Evaluate generalization to unseen classes, including region-specific signs (e.g., Indian "CATTLE" sign)

## 🏁 Results

| Model            | Train Accuracy | Test Accuracy |
|------------------|----------------|----------------|
| CNN              | 99.24%         | 96.12%         |
| ResNet18         | 99.94%         | **97.46%**     |
| MobileNetV3      | **99.98%**     | 96.80%         |
| EfficientViT v2  | 99.93%         | 97.24%         |
| ConViT-Tiny      | 99.87%         | 96.85%         |

✅ **Best test performance:** ResNet18 ProtoNet  
🔥 **Best training accuracy:** MobileNetV3 ProtoNet

## 🔍 Key Features

- Supports dynamic addition of new traffic sign classes (like Indian-specific signs) without retraining
- High generalization with few labeled examples
- Lightweight and scalable for real-world autonomous systems


