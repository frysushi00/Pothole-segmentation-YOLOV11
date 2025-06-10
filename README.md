# 🕳️ POTHOLE DETECTION & SEGMENTATION WITH YOLOV11 🕳️
This project contains a custom-trained YOLOv11 segmentation model for detecting **potholes** in road images and videos. The model was trained using annotated data and optimized specifically for high-accuracy pothole localization. **YOLO (You Only Look Once)** is a state-of-the-art object detection algorithm known for its speed and accuracy.

## 📌 Features
- **Pothole Detection:** Identifies the presence and location of potholes in images/videos using bounding boxes.
- **Pothole Segmentation:** Provides pixel-level masks for each detected pothole, offering precise shape and area information.
- **Video Processing: **Capable of processing video files (upload from local, or use existing files in Colab).
-** Results Visualization:** Displays the processed video with detected bounding boxes and segmentation masks directly within the notebook.

## 📦 Model Details
- **Model Type:** YOLOv11 with Segmentation Head (YOLOV11-Seg)
- **Trained for:** Pothole Detection
- **Framework:** Ultralytics YOLO
- **Input:** Images or videos of roads
- **Output:** Segmentation masks highlighting pothole regions

## 🛠 Core workflow
- Environment Setup: Installs necessary libraries, including ultralytics for YOLOv11.
- Model Loading: Loads a pre-trained YOLOv11-Seg model that I custom-trained specified for potholes and patches segmentation.
- Inference: The YOLOv11-Seg model performs real-time detection and segmentation on the input video.

## 🧪 How to Use
### 1. Load the model
```python
from ultralytics import YOLO
model = YOLO("best.pt")
```

### 2. Run on image
```python
results = model("your_image.jpg", task="segment")
results[0].show()
```
### 3. Run on video
```python
results = model("your_video.mp4", task="segment", save=True)
```

## 📊 Training Summary
- 10 Epochs in 0.041 hours
- Results : <br>
  ![image](https://github.com/user-attachments/assets/928cf940-ac82-40a1-9788-332b9f2d2a44)
  ![image](https://github.com/user-attachments/assets/d2ad5b97-5ef4-4dda-a048-967a7b36a0ad)
  ![image](https://github.com/user-attachments/assets/114f9ce3-7dac-4831-9e29-90295fbb4603)

## 🚀 Deployment
frysushiws/pothole-segmentation-yolov11-v2 <br>
**LICENSE :** AGPL-3.0

## Reference 📚
> Linas Kondrackis. (Oct 3, 2024). How to Train YOLOv11 Instance Segmentation on a Custom Dataset. Roboflow 
> [Blog](https://blog.roboflow.com/train-yolov11-instance-segmentation/)  
