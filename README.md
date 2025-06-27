
# 🚦 RoadRadar: Real-Time Speed Detection with Python, OpenCV, and YOLOv8

This project focuses on real-time vehicle detection, speed estimation, and violation alerting from video footage using Python, OpenCV, and the YOLOv8 object detection model. It showcases how deep learning models and computer vision techniques can be integrated into a traffic surveillance pipeline to analyze road activity efficiently.

The system reads videos frame-by-frame, detects different vehicle types, estimates their speeds using bounding box dimensions, flags overspeed violations, and logs this information into CSV files. Annotated videos, frame snapshots of violations, and visual insights help understand vehicle behavior on roads — useful for smart city projects, traffic monitoring, or transportation research.

---

## 🎯 Key Objectives

- Detect vehicles using YOLOv8 object detection  
- Estimate speed using bounding box dimensions  
- Flag and log overspeeding vehicles  
- Annotate videos with color-coded bounding boxes and speed overlays  
- Export both full video and violation snapshots  
- Generate CSV logs and interactive analytics in Jupyter Notebook  

---

## ✅ Features

- Annotates video frames with vehicle type and estimated speed  
- Red-colored boxes for overspeeding vehicles  
- Color-coded bounding boxes for car, truck, bus, bike, etc.  
- Saves annotated video and alert images  
- Exports `speed_log.csv` and `speed_alert_log.csv`  
- Interactive charts and insights from logs  
- Designed for modularity and educational clarity  

---

## 📦 Input & Output

- **Input:** Raw traffic video (e.g., `sample_video.mp4`)  
- **Output:**
  - 📹 `processed_speed_video.mp4` – Annotated full video  
  - 🖼️ Alert frames in `output/alerts/` folder  
  - 📊 `speed_log.csv` – All detections with speed  
  - 🚨 `speed_alert_log.csv` – Only overspeeding records  

---

## 🚀 Highlights

- **YOLOv8-based detection** ensures fast and accurate object recognition  
- **Simple speed estimation** using bounding box logic  
- **TQDM progress bar** for real-time tracking in notebook  
- **CSV-based logging** for external analytics or dashboards  
- **Interactive visualizations** with matplotlib & pandas  
- **Notebook modularity**: clean, organized steps for each task  

---

## 🧱 Folder Structure

```
RoadRadar-Real-Time-Speed-Detection-System/
│
├── input/
│   └── sample_video.mp4                   # Original video
│
├── output/
│   ├── processed_speed_video.mp4          # Annotated full-length video
│   ├── speed_log.csv                      # All detections with speeds
│   ├── speed_alert_log.csv                # Only overspeed entries
│   └── alerts/
│       ├── alert_frame_001.jpg            # Snapshots of overspeeding vehicles
│       └── ...
│
├── yolov8n.pt                             # Pretrained YOLOv8n weights
├── requirements.txt                       # Required Python libraries
├── .gitignore                             # Git ignore rules
├── README.md                              # 📄 Project documentation (this file)
├── venv/                                  # (optional) virtual environment
│
├── 1_VideoSetupAndPreprocessing.ipynb     # Trim/prepare video input
├── 2_ObjectDetectionAndTracking.ipynb     # Vehicle detection + speed overlay
├── 3_SpeedAlertSystemAndAnalysis.ipynb    # Alert frame extraction
├── 4_SpeedViolationAnalysis.ipynb         # Visual insights from logs
```

---

## 🧰 Technologies Used

- Python  
- OpenCV  
- YOLOv8 (`ultralytics`)  
- Pandas  
- Matplotlib  
- TQDM (for progress bars)  
- Jupyter Notebook  

---

## 📊 Sample Visuals

### Annotated Video Frame  
- Shows: `Vehicle Type | Speed`  
- Color:  
  - Green: Normal  
  - Red: Overspeed  
  - Other colors for vehicle types

### Violation Snapshots  
Captured images when vehicle exceeds speed threshold.

---

## 🔮 Future Enhancements

- Calibrate bounding box width to real-world speed using perspective or GPS  
- Integrate license plate recognition for vehicle identification  
- Extend tracking across frames for speed smoothing  
- Export alerts to a dashboard or web application (Flask/Streamlit)  
- Convert CSV to YOLO/COCO format for training models  

---

> 🛠️ Built for traffic analysis, AI experimentation, and educational clarity by **Raj Kumar**.  
> GitHub: [@RajKumaar123](https://github.com/RajKumaar123)
