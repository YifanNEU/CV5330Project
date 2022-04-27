# Traffic Volume Detection and Prediction by Deep Learning Object Detection
CV5330 Final Project Yifan Li and Zhengtian Zhang
## 1. Introduction
As increasing attention of building a smart city with smart traffic, we are introducing a method of detecting and predicting the crowdedness in the aspect of traffic volume the information captured by traffic cameras. We will be using deep learning techniques and training an object detection model with in YOLOv5 framework. We will be developing the prediction model from real world traffic data and visualize the result.

## 2. Model Training
We applied the <a href="https://github.com/ultralytics/yolov5">YOLOv5</a> framework wo train our model. All training codes will be contained in CV5330_Project_Training.ipynb. 
The Dataset we used for training will be a combination of the public vehicle open image dataset from <a href="https://public.roboflow.com/object-detection/vehicles-openimages">RoboFlow</a> and images from traffic camera images in <a href="https://vancouver.ca/streets-transportation/traffic-cameras.aspx">City of Vancouver</a> website.
The training setting will be running 100 epochs with a batch size of 32 and IoU threshold of 0.5. This running time for a training will be 2.5 to 3 hours.

our model will be tested by detecting the images from the test set, the detailed result images can be found in the<a href="https://github.com/YifanNEU/CV5330Project/tree/main/train/runs/detect/exp">/train/runs/detect/exp</a> folder.

## 3. Prediction Model
We will be developing the prediction model based on the real-world traffic camera data. For this demo, we are using this YouTube video <a href="https://www.youtube.com/watch?v=wqctLW0Hb_0">Road traffic video for object recognition</a> as the resources. 
Our prediction is divided into two parts. The video will be divided into reference set and prediction set, with image captured from the video. The reference set will be used to determine the threshold for identifying the traffic volume into low, mid and high. At this stage, the thresholds are determined manually. We will be counting the bonding boxes detected by our trained model and utilize the counting information for thresholds.
The prediction set are images randomly captured from the same video and we applied the thresholds to predict the traffic volume captured in the image. The result will be visualized adding the volume indication and the counting result.

## 4. Result and Visualization
We generated images as stated in the previous section for the visualizations. Combining the images we also generated an animation of the images for a better visualization effect. Detailed images and gif image can be found in the<a href="https://github.com/YifanNEU/CV5330Project/tree/main/predict%20set%20final">main</a> folder.
