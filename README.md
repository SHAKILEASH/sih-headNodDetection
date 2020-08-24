# sih-headNodDetection
Done as a part of Smart India Hackathon 2020
# Head Nod Detector
This is a Python code which detects a person's head nod movement. Let us say if a person moved his/her head towards x-axis, the detector would display the gesture as NO, similarly if the movement was towards y-axis, the gesture is detected as YES. Coded using OpenCV library. For Detecting the head
nod gesture we use Lucas-Kanade Optical flow. Optical flow is the pattern of
apparent motion of image objects between two consecutive frames caused by
movement of objects. We do this by finding the midpoint of the face. The
pattern of apparent motion of the midpoint is then observed, if there is an
aggressive movement in x-axis and a mild movement in y-axis then the Gesture
Detected is “No”. Similarly, if there is an aggressive movement in y-axis and a
mild movement in x-axis then the Gesture Detected is “Yes”. There is a chance
that future point may disappear in the image, so the optical flow finds the next
point which may look closer to it. Therefore, to avoid this, we find the midpoint
to be tracked for every twelve frames.

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
 * OpenCV library - pip install opencv-python
