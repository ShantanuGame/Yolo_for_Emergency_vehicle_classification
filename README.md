#🚨 YOLOv5 Custom Emergency Vehicle Detection Model
##This project features a custom-trained YOLOv5 model designed specifically to detect emergency vehicles in real-time traffic scenarios. It is a crucial component of a Smart Traffic Management System, aimed at dynamically adjusting signal timings when emergency vehicles are detected, ensuring faster clearance and improved urban mobility.

##🔍 Model Overview
###Model Type: YOLOv5 (You Only Look Once - v5)
###Architecture: yolov5s (small variant)
###Training Framework: PyTorch
###Purpose: Detect 5 classes of vehicles with a focus on emergency response:
### 0 ambulance
### 1 fire_truck
### 2 police_car
### 3 bus
### 4 van

##📂 Dataset
###Source: Custom dataset collected and annotated from Roboflow

##Format: YOLOv5-compatible structure with:

###images/train, images/valid, images/test

###labels/train, labels/valid, labels/test

###data.yaml file with class names and paths

##📊 Performance
###Metric	Value
###mAP@0.5	53.5%
###mAP@0.5:0.95	37.0%
###Ambulance Precision	64%
###Ambulance Recall	84%

###Trained for 100 epochs on a GPU (T4) using Google Colab.

##🔧 Usage
###To run detection:

###python detect.py \
  ###--weights path/to/best.pt \
  ###--source path/to/image_or_video \
  ###--conf 0.25 \
  ###--save-txt \
  ###--save-conf \
  ###--device 0  # or 'cpu'
###🚦 Smart Signal Integration
###When emergency vehicles are detected:

###Triggers audio alert

###Overrides traffic lights: emergency lane gets priority

###Sets cooldown to avoid redundant signals
