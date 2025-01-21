# Object Detection Shooting Game Agent

This repository contains the code for creating an object detection-based shooting game agent using YOLOv11. The agent detects and classifies objects as **allies** or **enemies** based on labeled training data. The implementation includes data preparation, model training, and inference for real-time gameplay scenarios.

---

## Features
- **YOLOv11 Detection**: Leveraged YOLOv11 for robust person detection.
- **Custom Classification**: Classified detected persons as "allies" or "enemies" based on training data.
- **Dataset Preparation**: Automated data preparation by extracting person detections from video files and labeling them based on the folder name.
- **Inference**: Real-time classification and gameplay decision-making using the trained YOLOv11 model.
- **Output Visualization**: Results, including detection and classification, are saved in the `output` folder.

---

## Directory Structure
```
object_detection_game_agent/
│
├── data/                # Dataset folder
│   ├── allies/          # Videos of allies
│   ├── enemies/         # Videos of enemies
│
├── yolov11/             # YOLOv11 files and configurations
│   ├── annotations/     # Labeled data in YOLOv11 format
│   ├── weights/         # YOLOv11 trained weights
│
├── notebooks/           # Jupyter notebook for the entire pipeline
│   ├── object_detection_agent.ipynb
│
├── output/              # Inference results
│   ├── ally_detections/ # Detected allies
│   ├── enemy_detections/# Detected enemies
│
├── README.md            # Documentation
```

---

## Steps to Reproduce

### 1. **Dataset Preparation**
- Place videos of **allies** in the `data/allies` folder.
- Place videos of **enemies** in the `data/enemies` folder.
- The notebook extracts frames, detects persons, and assigns labels based on the folder name.

### 2. **Model Training**
- The notebook prepares the labeled data in YOLOv11 format.
- Train YOLOv11 using the prepared dataset to distinguish between allies and enemies.

### 3. **Inference**
- Use the trained YOLOv11 model for real-time inference.
- Detect and classify persons in new video inputs.
- Results are stored in the `output` folder.

---

## Requirements
Install the required dependencies:
```bash
pip install -r requirements.txt
```

### Major Dependencies:
- Python 3.8+
- ultralytics
- OpenCV
- PyTorch
- Matplotlib

---

## How to Run
1. Clone this repository:
```bash
git clone https://github.com/yourusername/object_detection_game_agent.git
cd object_detection_game_agent
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open the notebook:
```bash
jupyter notebook notebooks/object_detection_agent.ipynb
```

4. Follow the steps in the notebook for:
   - Data preparation.
   - Training the YOLOv11 model.
   - Running inference.

---

## Results
- Inference outputs, including bounding boxes and classifications, are stored in the `output` folder.
- Visualizations for allies and enemies detections are saved separately.

---

## Contributions
Feel free to contribute to this project by opening issues or submitting pull requests.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
