# SLAM

### Description
SLAM(Simultaneous localization and mapping) from a motorcar implemented in python.

### Particle Filter SLAM

<img src="https://user-images.githubusercontent.com/15256774/111953680-4ce69800-8b2a-11eb-8da5-4f143843cd8f.gif" width="400" height="400"/><img src="https://user-images.githubusercontent.com/15256774/111953981-bff00e80-8b2a-11eb-8935-2e2b1d1d62e6.gif" width="400" height="400"/>

- \[left\] Real images over time
- \[right\] Estimated trajectory (green), particles (red), estimated empty space (white), and estimated objects (grey) over time by particle filter SLAM

![fig1](https://user-images.githubusercontent.com/15256774/111969836-000cbc80-8b3e-11eb-995d-fe5894239c1a.png)
Figure 1: Sensor layout on the autonomous vehicle. We will only use data from the wheel encoders, fiber optic gyro (FOG), front 2D LiDAR (Middle SICK), and the stereo cameras.
