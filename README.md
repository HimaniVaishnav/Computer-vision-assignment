# YOLOV5
# **Original Repo**
[https://github.com/ultralytics/yolov5.git](https://github.com/ultralytics/yolov5.git)

# Quick Start Examples

## Install

Python>=3.6.0 is required with all [requirements.txt](requirements.txt) installed including PyTorch>=1.7: 

$ git clone https://github.com/HimaniVaishnav/YOLOV5.git  
$ cd yolov5  
$ pip install -r requirements.txt  

## Data Preparation

- As given data in coco format, for converting data into coco to yolo run this file [general_json2yolo.py](https://github.com/HimaniVaishnav/YOLOV5/blob/main/coco_to_yolo/general_json2yolo.py)
- Will get .txt file for each .jpg, structure should be as follows:  

.
├── ...
├── YOLOV5                    # Test files (alternatively `spec` or `tests`)
│   ├── benchmarks          # Load and stress tests
│   ├── integration         # End-to-end, integration tests (alternatively `e2e`)
│   └── unit                # Unit tests
└── ...

      



