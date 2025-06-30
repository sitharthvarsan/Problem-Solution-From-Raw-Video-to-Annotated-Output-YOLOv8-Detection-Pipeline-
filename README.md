# **YOLOv8 Video Object Detection**  
*Real-time object detection on videos using Ultralytics YOLOv8 in Python.*

---

## 🚀 Key Features  
- Frame-by-frame object detection  
- Bounding box annotations (class, confidence)  
- Supports MP4, AVI, webcam input  
- Jupyter Notebook compatible  

## ⚙️ Tech Stack  
| Component       | Purpose                     |
|-----------------|-----------------------------|
| YOLOv8          | Object detection model      |
| OpenCV          | Video processing & visualization |
| IPython         | Display video in Jupyter    |

## 📋 Quick Start  
1. Install dependencies:  
   ```bash
   pip install ultralytics opencv-python
   ```
2. Run detection:  
   ```python
   from ultralytics import YOLO  
   model = YOLO("yolov8n.pt")  
   results = model.predict("input.mp4", save=True)
   ```

## 🎯 Core Concepts  
- **Model Loading**: Pretrained YOLOv8 (nano/small/medium).  
- **Video Processing**:  
  - OpenCV for frame extraction/writing.  
  - `model.predict()` for batch inference.  
- **Visualization**:  
  - `results[0].plot()` for annotated frames.  

## 📂 Output Structure  
```
results/  
└── predict/  
    ├── input.mp4          # Annotated video  
    └── labels/            # Per-frame detection logs  
```

## 💡 Pro Tips  
- Use `device=0` for GPU acceleration.  
- Adjust `conf=0.5` to filter detections.  
- For webcam: `source=0`.  

## 🛠️ Troubleshooting  
- **Video not loading**: Check file paths.  
- **Low FPS**: Reduce `imgsz=320`.  
- **CUDA errors**: Verify GPU drivers.  
```



