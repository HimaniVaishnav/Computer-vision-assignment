## Computer vision assignment 

### (1) Install neccessary libraries

      
Run following commands to clone repository and to install necessary python packages

      git clone https://github.com/HimaniVaishnav/YOLOV5.git  
      cd yolov5  
      pip install -r requirements.txt  

- Python>=3.6.0
- PyTorch>=1.7: 

### (2) Prepare data to train yolo v5 model -> convert coco labels to yolo labels)
- Run following commands to convert coco labels to yolo format.

      cd yolov5/coco_to_yolo

- Download data from this [link](https://evp-ml-data.s3.us-east-2.amazonaws.com/ml%20interview/openimages-personcar/trainval.tar.gz)
- Edit general_json2yolo.py and replace D:/crap/Eagleview/trainval/annotations/ with the downloaded data path
- Run following command to convert coco data to yolo

      python general_json2yolo.py

- example converted data format

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
      
- or use the following [link](https://drive.google.com/file/d/1NH1TQOuChONS_L4GPvX272eVOeCwvYyZ/view?usp=sharing) to get postproccessed data


### (3) Training and inferencing Yolov5 mode;l on custom data

- Run jupyter notebook server and open [training_and_inference.ipynb](training_and_inference.ipynb) to train and run inference    
- We are using yolov5s which is very light weight in terms of computation.                                                             
                                                                                          
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

      - Data should be clean.
      - Annotations should be clean and accurate.
    
### False positives / accuracy matrics
     
      - train/box_loss = 0.043275, train/obj_loss = 0.059046, train/cls_loss = 0.004394, metrics/precision = 0.72551, metrics/recall = 0.63549, metrics/mAP_0.5 = 0.67286, val/box_loss = 0.044721, val/obj_loss = 0.04888, val/cls_loss = 0.005526
      
### Conclusion

      - Have used most light weigth pretrained model of YOLOv5 i.e. yolov5s after fined tuning the model on custom dataset got only 14mb weight file.
      - Have trained on 20 epochs with 16 batch size and time taken was 43 minutes.
      - lightweight model is used, which helps to reduce gpu usage while deployment.
      - model is perfroming well even on the person and car occlusions.
      
      
### Inference images [link](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp)      
  ![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp/image_000000113.jpg)
  ![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp/image_000000144.jpg)
  ![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp/image_000000149.jpg)
  ![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp/image_000000216.jpg)
  ![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp/image_000000221.jpg)
  ![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp/image_000000365.jpg)
  ![alt tag](https://github.com/HimaniVaishnav/YOLOV5/blob/main/runs/detect/exp/image_000000180.jpg)
      
      
      


      
      
      
                            
                           



      



