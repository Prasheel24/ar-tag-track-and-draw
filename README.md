# ENPM673 Project 1 -
AR Tag Detection | Homography | Warping | Lena Superimpose | Virtual Cube Projection

## Authors
* Prasheel Renkuntla
* Raj Prakash Shinde
* Shubham Sonawane
 
## Description
The project demonstrates AR Tag Detection, Homography and Warping to superimpose Lena image on the Tag.  Also, it projects a virtual cube on top of the tag.

## Dependencies
* Ubuntu 16
* Python 3.7
* OpenCV 4.2
* Numpy
* copy
* sys
* argparse

## Run
To run the detection, lena super impose and to draw a cube on a video with single tag -

```
python3.7 detection_tracking_ARTAG.py --vid Tag0.mp4 --func 1
```
For video with multiple tags, run the below command -
```
python3.7 detection_tracking_multi.py --vid multipleTags.mp4 --func 1
```

Options for "vid" argument -
* path to the video file

Options for "func" argument -
* 1 - to detect tag id and orientation
* 2 - to superimpose lena
* 3 - to draw a virtual cube on top of the tag

Input 1 or 0 in the command window (when prompted) to save into a video file
 
## Reference
* https://github.com/hughesj919/HomographyEstimation/blob/master/Homography.py
* https://www.owlnet.rice.edu/~elec539/Projects97/morphjrks/warpsri.html
