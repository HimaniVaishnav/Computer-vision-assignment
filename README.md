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

      $ python path/to/detect.py --source path/to/img.jpg --weights best.pt --img 640 --conf 0.25
                             OR
      $ python detect.py --source 0  # webcam
                            file.jpg  # image 
                            file.mp4  # video
                            path/  # directory
                            path/*.jpg  # glob
                            'https://youtu.be/NUsoVlDFqZg'  # YouTube
                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
                            
- Run commands below to reproduce results on custom dataset.Use the largest --batch-size your GPU allows (in colab can use 16 batch-size).  

       $ python train.py --img 640 --batch 16 --epochs 20 --data data.yaml --weights yolov5s.pt --cache  
                                                                                     yolov5m.pt                                
                                                                                     yolov5l.pt                                
                                                                                     yolov5x.pt 
                                                                                          
                                                                                          
## Results

![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/train/exp/val_batch2_pred.jpg)


## About the model

### Model Name
      
      YOLOv5
 
### Links to dataset and framework

      https://evp-ml-data.s3.us-east-2.amazonaws.com/ml interview/openimages-personcar/trainval.tar.gz 
     
### About the model

      - YOLOv5 is a family of object detection architectures and models pretrained on the COCO dataset
      - YOLOv5 an acronym for 'You only look once', is an object detection algorithm that divides images into a grid system. Each cell in the grid is responsible for detecting      objects within itself.
      - YOLOv5 is one of the most famous object detection algorithms due to its speed and accuracy.
      
### Primary Analysis

      - Removing irrelevant images e.g. blurr, half portion of person or class.
      - Removing duplicate data.
     
### Assumptions

      - Annotations should be proper and clear.
      - In image focus should be on classes (instance to be detected) rather than other instance.
    
### False positives
      
      - A false positive is an outcome where the model incorrectly predicts the positive class.
      - In our model 
      
### Conclusion

      - Have used most light weigth pretrained model of YOLOv5 i.e. yolov5s after fined tuning the model on custom dataset got only 14mb weight file.
      - Have trained on 20 epochs with 16 batch size and time taken was 43 minutes.
      - learning rate = 0.0021958, train/box_loss = 0.043275, train/obj_loss = 0.059046, train/cls_loss = 0.004394, metrics/precision = 0.72551, metrics/recall = 0.63549, metrics/mAP_0.5 = 0.67286, val/box_loss = 0.044721, val/obj_loss = 0.04888, val/cls_loss = 0.005526
      
### Recommendations


      
      
      
                            
                           



      



