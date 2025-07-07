# PPE Detection with YOLOv8

This project implements a real-time PPE (Personal Protective Equipment) detection system to monitor safety compliance in industrial environments. Using a fine-tuned YOLOv8 model, the system detects individuals wearing helmets and vests and alerts when safety gear is missing.

---

## 📌 Features

- Detects key PPE: **helmets** and **vests**
- Identifies missing gear in real-time from live camera feeds
- Provides on-screen alerts and visual feedback
- Designed for deployment in factory, warehouse, or construction environments
- Lightweight model suitable for edge devices like Jetson Xavier NX

---

## 📁 Dataset

- **Source**: Captured in industrial-like settings
- **Classes**: `person`, `helmet`, `vest`
- **Labeling & Management**: Done using **Roboflow**
- **Preprocessing & Augmentation**:
  - Image resizing
  - Horizontal flipping
  - Rotation
  - Contrast adjustment

---

## 🧠 Model Training

- Fine-tuned a pre-trained **YOLOv8s** model on the custom dataset
- Training conducted for 50 epochs with 640×640 resolution
- Achieved high precision and recall on validation set
- Best-performing model weights saved and used for inference

---

## 📊 Evaluation Metrics

| Metric     | Result (approx.) |
|------------|------------------|
| mAP@0.5    | 0.89             |
| Precision  | 0.91             |
| Recall     | 0.87             |

- Evaluated using confusion matrix and per-class performance
- Verified detection reliability under different lighting and angles

---

## 🚀 Deployment

- Model deployed for real-time inference using a webcam feed
- Integrated with **OpenCV** for video streaming and annotation
- System alerts when any required PPE (helmet or vest) is missing
- Designed to integrate with broader ROS or IoT safety monitoring systems

---

## 🖥️ System Requirements

- Python 3.8+
- YOLOv8 (Ultralytics)
- OpenCV
- NumPy
- Roboflow (for dataset management)


