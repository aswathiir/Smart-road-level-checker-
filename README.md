# Road Surface Analysis and Visualization

## Overview
This project aims to develop a cost-effective road surface analysis system using **Intel RealSense RGB-D cameras** instead of LiDAR. The system will classify road features such as speed bumps, flower beds, and pedestrian walkways based on length thresholds while analyzing potholes. The collected data will be visualized using **RViz and Gazebo**, with Kalman filtering for sensor fusion and noise reduction.

## Hardware Components
1. **Intel RealSense RGB-D Camera** – Captures depth and color data for road surface mapping.
2. **IMU (MPU-6050)** – Provides orientation and inclination readings for accurate road profiling.
3. **Raspberry Pi** – Serves as the primary computation unit for processing sensor data.

## Tech Stack
1.**Backend**: Flask (Python).
2. **Frontend**: Bootstrap, Jinja2.
3.**Visualization**: Matplotlib, Plotly, Open3D (for 3D point clouds).
4.**Data Handling**: NumPy, Pandas (for processing simulated depth data).
5.**Communication**: Flask REST API (later WebSockets/MQTT for real-time updates).

## Methodology
1. **Data Acquisition**:
   - The **Intel RealSense camera** captures RGB and depth information of the road surface.
   - The **IMU (MPU-6050)** provides orientation and inclination data to correct any distortions.

2. **Preprocessing & Filtering**:
   - A **Kalman Filter** is applied to fuse IMU and camera data, reducing noise and improving accuracy.
   - Depth data is analyzed to differentiate road elements like speed bumps and potholes.

3. **Feature Classification & Thresholding**:
   - Predefined length thresholds categorize road elements (e.g., a feature of a certain width and height is classified as a speed bump or pedestrian crossing).
   - Pothole analysis is done using depth variance and pixel-based methods.

4. **Simulation & Visualization**:
   - **Gazebo** is used to simulate the 3D road environment and test the system virtually before deployment.
   - **RViz** displays real-time sensor data and road surface mapping.

## Workflow
1. **Data Collection**
   - Intel RealSense captures RGB-D data.
   - IMU provides orientation and inclination readings.

2. **Processing & Filtering**
   - Kalman Filter fuses IMU and depth data for better accuracy.
   - Noise reduction and correction are applied.

3. **Feature Extraction & Classification**
   - Thresholding techniques classify road features (e.g., speed bumps, pedestrian crossings, potholes).

4. **Simulation & Visualization**
   - Processed data is fed into **Gazebo** for virtual simulation.
   - **RViz** visualizes real-time sensor outputs.


## Deployment Considerations
- **Embedded System:** Raspberry Pi or Jetson for edge processing.
- **Real-Time Processing:** Optimized code to process data efficiently.
- **Integration with ROS:** Ensuring seamless communication between hardware components and visualization tools.

## Conclusion
This project replaces LiDAR with **Intel RealSense RGB-D cameras** for a low-cost, efficient road analysis system. Using **Kalman Filtering**, **RViz**, and **Gazebo**, the system accurately identifies road features while providing real-time visualizations.

