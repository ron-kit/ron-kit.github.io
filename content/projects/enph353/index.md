+++
image = "edge detection.png"
date = "2025-01-17"
title = "Simulated Self-Driving Robot"
type = "gallery"
+++

A virtual robot that detects features and navigates terrain to compete in a race. Programmed with OpenCV, connected with ROS, and simulated in Gazebo.

---

## Competition Map

{{<image src="353map.gif">}}

## Development Log

I started with a very basic prebuilt robot, not much more than a box on wheels, and developed a system to detect the road. 
The standard approach to this is to apply a Gaussian blur followed by a binary threshold, but I opted for HSV thresholding instead (seen in the cover image), which procured a very strong boundary between road and ground.

{{<video src="tracked_video_feed.mov">}}

Using a pregenerated video of the robot driving a lap, I added realtime frame processing to locate the the road.
By taking the centroid of the road segment detected in the bottom quarter of each frame, my algorithm was able to very accurately place a circle on the middle of the road. 

This would be useful for navigation later, but for now I pivoted to another task: keypoint detection with SIFT.

---

{{<image src="keypoints.png">}}

I made a basic UI in Qt to import reference images and track my camera feed. \
Using SIFT I located and displayed the keypoints (small regions with a transformation-invariant color gradient) on the live feed.
Invariance is a pretty abstract classification but it seems to pick out centers (as seen on the lights) and edges (as seen on me) most often.

{{<image src="snickers-recognized.png">}}

A point mapping from reference to frame is dynamically generated using Flann (method of locating closest vector pairs in gradient space) 
and RANSAC (a probabilistic sampling technique). Finally a homography is drawn to highlight the detected image. \
Here it is recognizing a photo of my cat, even under a slight skew.

---

To lay the foundation for CNNs I followed alongside Karpathy's tutorial on gradient descent 
and used it to make a simple linear regression generator with a squared difference loss function.

The application of this project was to text detection. Building off TensorFlow features I developed and trained a deep learning MLP network.
With only 20 epochs of training it reached about 90% accuracy in classifying letters and numbers.

[TODO: CONFUSION MATRIX HERE]

---

Having implemented these sub-behaviours I approached the real challenge: training the robot to navigate through the environment.

There are many variables at play here: the road changes height, material, and color, and obstacles, both rigid and moving, hinder the robot's movement.

I made a basic Q-learning system to start, using the HSV thresholding from before.
The learning is implemented with the Bellman equation, which uses the following parameters:

- Alpha: learning rate.
- Gamma: value of observation relative to known rewards.
- Epsilon: exploration factor.

{{<image src="robot_improving.png">}}

With a simple, static reward function, as well as a pretty high epsilon, the robot is nevertheless able to learn and improve. The rewards plot is a bit erratic as the robot randomly veers off the track in tireless pursuit of escaping local minima, but exhibits a clear upward trend.

