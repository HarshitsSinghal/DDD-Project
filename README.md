## Overview

Driver fatigue is one of the major causes of road accidents worldwide.  
This project proposes an efficient, real-time driver fatigue detection system using MobileNetV2 and face-centric transfer learning techniques.  
The lightweight yet powerful model can be deployed in real-world scenarios to enhance road safety.  
This work is part of a research paper submitted to Springer for publication.

---

## Features

- Real-time driver fatigue detection  
- Lightweight MobileNetV2 architecture optimized for edge deployment  
- Face-centric transfer learning for improved accuracy  
- Handles edge cases with custom self-collected images  
- Achieves 91% accuracy on a combined dataset of 4,000+ images

---

## Dataset

We used a combined dataset from multiple open-source sources and augmented it with self-captured images to improve edge-case handling.  

**Total Images:** ~4,000  
**Classes:**  
   ---Drowsy  
   ---Non-Drowsy  

**Data Preprocessing:**  
- Face detection and cropping using MediaPipe  
- Augmentation (rotation, zoom, flips, etc.)  
- Normalization and resizing to 224x224

---

## Model Architecture

- **Base Model:** MobileNetV2 (Transfer Learning)  
- **Input Shape:** 224 x 224 x 3  
- **Preprocessing:** MediaPipe-based face detection + augmentation  
- **Optimizer:** Adam  
- **Loss Function:** Binary Crossentropy  
- **Metrics:** Accuracy, Precision, Recall, F1-score  
- **Final Layers:**  
    - GlobalAveragePooling2D  
    - Dense(128, activation='relu')  
    - Dropout(0.5)  
    - Dense(1, activation='sigmoid')

---

## Research Paper

This work is based on the research paper:  
"Efficient Driver Fatigue Detection via Face-Centric Transfer Learning with MobileNetV2"  
Submitted to Springer, 2025
