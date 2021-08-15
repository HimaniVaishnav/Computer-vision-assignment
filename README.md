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

      YOLOV5  
      ├── data  
      │   └── dataset  
      │       ├── images   
      │       │   ├── train (80% .jpg file)  
      │       │   ├── val   (20% .jpg file)  
      │       ├── labels  
      │       │   ├── train (80% .txt file)  
      │       │   ├── val   (20% .txt file)    
      └── ...
      
or use the following link to download dataset folder directly from google drive and paste it into [data](data) folder:

[https://drive.google.com/file/d/1NH1TQOuChONS_L4GPvX272eVOeCwvYyZ/view?usp=sharing](https://drive.google.com/file/d/1NH1TQOuChONS_L4GPvX272eVOeCwvYyZ/view?usp=sharing)

## Training and Inference 

- Run [training_and_inference.ipynb](training_and_inference.ipynb) for training and inference
- Also can use [detect.py](detect.py) for inference, folder will be generate for all detected images [run/detect/exp/]([run/detect/exp/])

      $ python path/to/detect.py --source path/to/img.jpg --weights best.pt --img 640
                             OR
      $ python detect.py --source 0  # webcam
                            file.jpg  # image 
                            file.mp4  # video
                            path/  # directory
                            path/*.jpg  # glob
                            'https://youtu.be/NUsoVlDFqZg'  # YouTube
                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
                         
                            
                           



      



