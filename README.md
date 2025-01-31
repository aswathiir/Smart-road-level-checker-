# Smart Road Level Checker

## Description
This project is a cost-effective road leveling and surface profiling system that utilizes **RPLIDAR** and **IMU sensors** to detect surface irregularities in real time. The system processes sensor data using **Kalman filtering** and **sensor fusion**, then visualizes results on **Grafana dashboards** for monitoring and analysis.

## Features
- **Real-time surface profiling** using RPLIDAR
- **IMU-based tilt and orientation correction**
- **Noise filtering with Kalman Filter**
- **Sensor fusion for accurate road leveling assessment**
- **Data visualization in Grafana**
- **ROS integration for automation and simulation in Gazebo**

## Technology Stack
- **Hardware**: RPLIDAR A2, MPU-6050 IMU, Raspberry Pi
- **Software**: ROS, Python, Open3D, PCL, Grafana, InfluxDB
- **Processing**: Sensor fusion, ground segmentation, and SLAM

## Workflow
1. **Connect RPLIDAR to ROS** using the `rplidar_ros` package.
2. **Visualize LiDAR data in RViz** for real-time scanning.
3. **Integrate IMU data** using the MPU-6050 Python library and publish as a ROS topic.
4. **Apply noise filtering** using the Kalman Filter.
5. **Fuse LiDAR and IMU data** with the `robot_localization` package.
6. **Run Hector SLAM** for mapping and test in RViz.
7. **Preprocess LiDAR data** using PCL for noise reduction.
8. **Use Open3D for ground segmentation** and remove non-ground points.
9. **Simulate the system in Gazebo** with sensor plugins.
10. **Deploy the system in real-world environments** and visualize results in Grafana.

## Use Cases
- Road and pavement surface assessment
- Construction site ground leveling
- Industrial surface profiling

## Installation
1. Install ROS and dependencies for RPLIDAR and IMU sensors.
2. Clone this repository and set up ROS workspace.
3. Launch the LiDAR and IMU nodes.
4. Run the Kalman Filter and SLAM for mapping.
5. Visualize data using Grafana.

## Future Enhancements
- Implementing adaptive sensor fusion for improved accuracy.
- Extending mapping capabilities for large-scale environments.
- Adding machine learning for automated surface classification.

## Contributors
- Aishwary Manoj - cb.sc.u4aie23211
- Aswathi Ranjith - cb.sc.u4aie23215
- Sanmita GJ - cb.sc.u4aie23215
- Lakshmi Ridhanya - cb.sc.u4aie23215

