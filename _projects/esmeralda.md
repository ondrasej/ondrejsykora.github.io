---
title: Esmeralda
layout: page
short: A camera-driven robot.
---
Esmeralda is a result of assignment project for the lecture Evolutionary Robotics at Faculty of Mathematics and Physics, Charles University. My goal was to create a camera-driven robot capable of following a ball or another object. Due to the lack of time (and to the difficulty of the task), I ended up having a static camera and a robot driving to a certain point specified in the camera image.

## Hardware

It is usual that the robots for the lecture are created using Lego Mindstorms (provided by the university). However, one had to use it at the university lab, which didn't suit me much, I prefer working at home, on my own. Fortunately, I was able to borrow and use the robot Ferda, created by the team Short Circuits. The camera was a standard Creative webcam, and I've used my laptop for processing the camera image, and controlling the robot.

## Locating the robot

Obtaining the hardware was simple enough, now I had to do something about the software. I've chosen to use OpenCV as a base, which proved to be a good choice. To easily locate the robot on the image from the camera, four balls of different colours were attached to the robot. Then, the color planes corresponding to the colours of the balls were extracted from the image, and the possible positions of the balls were extracted from them. The most likely position of the robot is calculated from these points, by matching balls of the right colors, which are not too far from each other. Nothing too smart, but it works just fine in simple environments.

## Navigation

Though the localization of the robot might look simple, the navigation is even simpler. The camera itself is static, and it is assumed to be looking at the environment from an elevated position. I've assumed even more - that there are no obstacles in the environment, and that the robot can get to any point. Under these assumptions it was easy to treat the environment as a simple 2D space, and steer the robot using the simplest algorithm possible. Turn to the destination. Go forward. Nothing too smart, but it works just fine in simple environments.
