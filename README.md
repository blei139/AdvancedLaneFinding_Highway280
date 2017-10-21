# AdvancedLaneFinding_Highway280
This repository is used for advanced lane finding technique which I learned from Udacity's self-driving car nanodegree program 
and the YOLO car detection, using YOLO object detection from littlegrass YOLO example for YOLO object detection.  The ipython 
scripts will take an input video, find the lane markers ahead, and identify the cars next to the ego vehicle.  The input video is taken 
from the border between Daly City and San Francisco on Highway 280 with a dash board camera.  

The advanced lane finding pipeline finds the lane markers for the ego car.  The advanced lane finding pipeline has 4 steps.  The steps are explained as follow: a) Calibrate the camera. b) Undistort the lane image. c) Warp the lane image to find the lanes. d) Unwarp the lane lines back to the original lane image.

The YOLO script is used to detect cars next to the ego vehicle.  The YOLO script uses Keras to compile the Yolo pipeline, next loads the YOLO weights file, uses the probability to classify the object belong to an object class, and finally uses bounding box to draw around
the object and identification label to identify the object.  Once the probability of that object class is higher than the minimum threshold,  the object is identified.  For example, the car has a class number of 6 and the minimum threshold is 0.7. 

Instruction to do the advanced lane finding and Yolo car detection:
1) Run vehicleDetectionAdvancedLaneFinding.ipynb in Anaconda to generate the advanced lane finding video.
2) Run YoloCarDetection.ipynb in Anaconda to identify the cars next to the ego car to generate the combined advanced lane finding and 
   car detection video.

Youtube video link:
https://youtu.be/yUzXih0IYdc
