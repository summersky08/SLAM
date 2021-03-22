# SLAM

### Description
[SLAM(Simultaneous localization and mapping)](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping) from a motorcar implemented in python.

### Particle Filter SLAM
Simultaneous localization and mapping (SLAM) based on [particle filter](https://en.wikipedia.org/wiki/Particle_filter#:~:text=Particle%20filtering%20uses%20a%20set,can%20take%20any%20form%20required.) using [odometry](https://en.wikipedia.org/wiki/Odometry), 2-D [LiDAR](https://en.wikipedia.org/wiki/Lidar) scans, and [stereo camera](https://en.wikipedia.org/wiki/Stereo_camera) measurements from an autonomous car. Odometry and LiDAR measurements are used to localize the robot and 2-D [occupancy grid map](https://en.wikipedia.org/wiki/Occupancy_grid_mapping) of the environment is also build.

<img src="https://user-images.githubusercontent.com/15256774/111973305-b32ae500-8b41-11eb-88eb-17f68ab933e9.gif" width="400" height="400"/><img src="https://user-images.githubusercontent.com/15256774/111973334-baea8980-8b41-11eb-9c7b-ba07595593a4.gif" width="400" height="400"/>
- \[left\] Real images over time
- \[right\] Estimated trajectory (green), particles (red), estimated empty space (white), and estimated objects (grey) over time by particle filter SLAM

- The vehicle is equipped with a variety of sensors. In this project, we will only use data from the front 2-D LiDAR scanner, [fiber optic gyro (FOG)](https://en.wikipedia.org/wiki/Fibre-optic_gyroscope), and encoders for localization and mapping as well as the stereo cameras for texture mapping. See Fig. 1 for an illustration.
  - The FOG provides relative rotational motion between two consecutive time stamps. The data can be used as ∆θ = τω, where ∆θ, ω, and τ are the yaw angle change, angular velocity, and time discretization, respectively.
  - The sensor data from the 2D LiDAR, encoders, and FOG are provided in .csv format. The first column in every file represents the timestamp of the observation. For the stereo camera images, each file is named based on the timestamp of the picture.
  - The goal of the project is to use a particle filter with a differential-drive motion model and scan-grid correlation observation model for simultaneous localization and occupancy-grid mapping.

<img src="https://user-images.githubusercontent.com/15256774/111969836-000cbc80-8b3e-11eb-995d-fe5894239c1a.png" width="700"/>
Figure 1: Sensor layout on the autonomous vehicle. We will only use data from the wheel encoders, fiber optic gyro (FOG), front 2D LiDAR (Middle SICK), and the stereo cameras.
