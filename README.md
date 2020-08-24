# sih-headNodDetection
Done as a part of Smart India Hackathon 2020
## Head Nod Detector
This is a Python code which detects a person's head nod movement. Coded using **OpenCV** library. For Detecting the head
nod gesture we use **Lucas-Kanade Optical flow**. Optical flow is the pattern of
apparent motion of image objects between two consecutive frames caused by
movement of objects. We do this by finding the midpoint of the face. The
pattern of apparent motion of the midpoint is then observed, if there is an
aggressive movement in x-axis and a mild movement in y-axis then the Gesture
Detected is **“No”**. Similarly, if there is an aggressive movement in y-axis and a
mild movement in x-axis then the Gesture Detected is **“Yes”**. There is a chance
that future point may disappear in the image, so the optical flow finds the next
point which may look closer to it. Therefore, to avoid this, we find the midpoint
to be tracked for every twelve frames.
## Concept 
The ideology behind the detector is as follows:
  * Detect the faces
  * Calculate the center of face
  * Capture the movement of the face center
  * For capturing the face center movement, Lucas Canade Optical Flow concept is used
## OpenCV Methods
  * Face Detection - detectMultiScale()
  * Face center movement - calcOpticalFlowPyrLK()
## Lucas-Kanade algorithm
The algorithm that we have used to detect the gesture is Lucas - Kanade optical flow.
     The Lucas-Kanade algorithm is an **efficient method** for obtaining optical flow information at interesting points in an image (i.e. those exhibiting enough intensity gradient information). 
     It works for moderate object speeds.
* The Lucas-Kanade optical flow algorithm is a simple technique which can provide an estimate of the **movement of interesting features in successive images** of a scene.
* We would like to associate a movement vector (u, v) to every such ”interesting” pixel in the scene, obtained by **comparing** the two consecutive images. 
* It works by trying to guess in which direction an object has moved so that local changes in intensity can be explained.<br />
![optical flow](https://docs.opencv.org/3.4/optical_flow_basic1.jpg)<br />
Optical flow works on several assumptions:
* The **pixel intensities** of an object **do not change** between consecutive frames.
* **Neighbouring** pixels have **similar** motion.

The Lucas-Kanade algorithm makes a **”best guess”** of the displacement of a neighborhood by looking at changes in pixel intensity which can be explained from the known intensity gradients of the image in that neighborhood. 
For a simple pixel we have two unknowns (u and v) and one equation (that is, the system is underdetermined). We need a neighborhood in order to get more equations. 
Doing so makes the system overdetermined and we have to find a least squares solution. The LSQ solution averages the optical flow guesses over a neighborhood.
## Requirements
 * OpenCV  (Open source Computer Vision) library for image processing
 * NumPy Package for handling array data

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

