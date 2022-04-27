# Traffic Volume Detection and Prediction by Deep Learning Object Detection
CV5330 Final Project Yifan Li and Zhengtian Zhang
## 1. Introduction
As increasing addtention of building a smart city with smart traffic, we are introducing a method of detecting and predicting the crowdedness in the sapect of traffic volume the information captured by traffic cameras. We will be using deep learning techniques and traning an object detection model with in YOLOv5 framework. We will be developing the prediction model from real world traffic data and visualize the result.

## 2. Model Training
We applied the <a href="https://github.com/ultralytics/yolov5">YOLOv5</a> framework wo train our model. All training codes will be contained in CV5330_Project_Training.ipynb. 
The Dataset we used for training will be a conbination of the public vehicle open image dataset from <a href="https://public.roboflow.com/object-detection/vehicles-openimages">RoboFlow</a> and images from traffic camera images in <a href="https://vancouver.ca/streets-transportation/traffic-cameras.aspx">City of Vancouver</a> website.
The traning setting will be running 100 epoches with a batch size of 32 and IoU threshold of 0.5. This running time for a training will be 2.5 to 3 hours.

our model will be tested by detecting the images from the test set, the detailed result images can be found in the<a href="https://github.com/YifanNEU/CV5330Project/tree/main/train/runs/detect/exp">/train/runs/detect/exp</a> folder.

## 3. Prediction Model
