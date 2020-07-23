# sih-headNodDetection
Done as a part of Smart India Hackathon 2020
# Head Nod Detector
This is a python code which detects a person's head nod movement. Let us say if a person moved his/her head towards x-axis, the detector would display the gesture as NO, similarly if the movement was towards y-axis, the gesture is detected as YES. Coded using OpenCV library.
# Concept 
The ideology behind the detector is as follows:
  * Detect the faces
  * Calculate the center of face
  * Capture the movement of the face center
  * For capturing the face center movement, Lucas Canade Optical Flow concept is used
# OpenCV Methods
  * Face Detection - detectMultiScale()
  * Face center movement - calcOpticalFlowPyrLK()
# Requirements
 * Python
 * OpenCV library 
