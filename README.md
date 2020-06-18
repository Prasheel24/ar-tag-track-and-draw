# AR Tag Detection and Virtual Cube Projection
Homography | Warping | Lena Superimpose

## Authors
* Prasheel Renkuntla
* Raj Prakash Shinde
* Shubham Sonawane
 
## Description
The project demonstrates AR Tag Detection, Homography and Warping.
A tag looks like below-
<p align="center">
<h5>Tag 0</h5>
<img src="/Code/ref_marker.png" width="70%">
</p>


Then Lena's image is superimposed on the Tag. Also, we project a virtual cube on top of the tag.


## Dependencies
* Ubuntu 16
* Python 3.7
* OpenCV 4.2
* Numpy
* copy
* sys
* argparse

## Run
First please change to the Code directory.

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

## Demo
The tag detected after processing with different filters is given below-
<p align="center">
<h5>Tag 0</h5>
<img src="/output/tag_0.png" width="70%">
</p>

Post processing this image, it is parsed to find the corresponding tag id (binary representation) and orientation, as given below-
<p align="center">
<h5>Terminal output for detection</h5>
<img src="/output/tagid_detect.png" width="70%">
</p>

After this detection, Lena is superimposed according to the orientation as found from before-
<p align="center">
<h5>Lena superimpose</h5>
<img src="/output/lena_tag0.png" width="70%">
</p>

Finally, we use the projection matrix to draw virtual cubes on top of these modified tags-
<p align="center">
<h5>Multiple tags with Cube projection</h5>
<img src="/output/multi_tag_cubes.png" width="70%">
</p>

The output folder contains results from detection of single tag only due to size restrictions.


## Reference
* https://github.com/hughesj919/HomographyEstimation/blob/master/Homography.py
* https://www.owlnet.rice.edu/~elec539/Projects97/morphjrks/warpsri.html
