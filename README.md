# waste-detection-yolov8
## 🗑AI-Based Waste Detection Using YOLOv8

A computer vision-based waste classification system built using YOLOv8 and OpenCV to detect and classify different types of garbage (e.g., plastic, metal, cardboard, organic) in real-time using a webcam. This project promotes sustainable recycling by automating waste sorting at the source.

---

## 🚀 Features

- 🧠 Object detection using YOLOv8
- 🎥 Real-time webcam-based waste detection
- 🗂️ Multi-class waste classification (plastic, paper, metal, glass, etc.)
- 🔄 Live bounding boxes and confidence scores overlay
- ⚙️ Custom trained YOLOv8 model

---

## 🛠️ Tech Stack

| Technology | Use |
|------------|-----|
| Python | Programming Language |
| YOLOv8 (Ultralytics) | Object Detection |
| OpenCV | Video Stream Processing |
| Roboflow / LabelImg | Dataset Annotation |
| PyTorch | Deep Learning Backend |

---

## 📊 Dataset

> ⚠️ **Note:** The dataset used is large and is **not included** in the repository due to file size constraints.

- **Source**: [Garbage Classification Dataset on Kaggle]
- **Classes**: Plastic, Metal, Cardboard, Glass, Organic, etc.
- **Format**: Images annotated in YOLO format

📥 Download and place the dataset in the `datasets/` folder before training or detection.

---

## 🧠 Model Training Workflow

1. **Dataset Annotation**: Using LabelImg or Roboflow in YOLO format
2. **Data Split**: Train/Val/Test (80/10/10)
3. **Model Training**: bash
   yolo task=detect mode=train model=yolov8n.yaml data=data.yaml epochs=50 imgsz=640
4. **Evaluation & Metrics**:
mAP (mean Average Precision)
Precision/Recall
Confusion matrix
5. **Real-Time Detection**: yolo task=detect mode=predict model=best.pt source=0
