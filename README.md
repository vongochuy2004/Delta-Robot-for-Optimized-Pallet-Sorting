# Vision-Based Delta Robot Palletizing System

An automated palletizing system integrating a Delta robot, Intel RealSense D415 depth camera, YOLO, OpenCV, and Mitsubishi PLC for vision-based object detection, 3D dimension measurement, pallet layout optimization, and robotic motion control.

## Overview

This project focuses on developing an automated palletizing solution for rectangular boxes using computer vision and industrial motion control.

An Intel RealSense D415 camera captures RGB and depth data to detect objects, estimate their dimensions and spatial positions, and determine their orientation. The processed information is used to calculate robot movements and optimize box placement on a pallet.

The system integrates a Delta robot with a Mitsubishi IQ-R PLC and RD77MS4 motion control module to coordinate robotic operations and automate the palletizing process.

## Key Features

- **Object Detection:** Detect rectangular boxes using YOLO.
- **Computer Vision:** Process images using Python and OpenCV for contour analysis, geometric refinement, and orientation estimation.
- **3D Dimension Measurement:** Combine RGB and depth information from the Intel RealSense D415 to estimate object dimensions.
- **Coordinate Transformation:** Convert camera-based measurements into robot coordinate positions.
- **Delta Robot Kinematics:** Calculate robot joint angles using inverse kinematics.
- **Pallet Layout Optimization:** Implement a 3D bin-packing-based approach to determine box placement and improve pallet space utilization.
- **Industrial Motion Control:** Communicate with a Mitsubishi IQ-R PLC and RD77MS4 motion module.
- **System Monitoring:** Provide an operator interface for monitoring system status and controlling operations.

## System Architecture

The system follows this processing pipeline:

1. **Image Acquisition:** Capture aligned RGB and depth frames using the Intel RealSense D415.
2. **Object Detection:** Identify rectangular boxes using YOLO.
3. **Dimension and Pose Estimation:** Analyze depth data and object contours to estimate dimensions, position, and orientation.
4. **Pallet Planning:** Calculate suitable box placement based on pallet dimensions, collision constraints, and stacking conditions.
5. **Robot Motion Calculation:** Compute the required Delta robot joint angles using inverse kinematics.
6. **PLC Communication:** Transfer motion commands and control data to the Mitsubishi PLC.
7. **Automated Palletizing:** Execute pick-and-place operations using a suction-based end effector.
<img width="866" height="479" alt="image" src="https://github.com/user-attachments/assets/c224273f-e37a-4d47-93bb-36d031c68a72" />


## Hardware

- Delta robot
- Intel RealSense D415 depth camera
- Mitsubishi IQ-R PLC
- Mitsubishi RD77MS4 motion control module
- Suction-based end effector
- Conveyor and associated control components
<img width="675" height="440" alt="image" src="https://github.com/user-attachments/assets/68dc3d07-db93-4ac9-9ac7-0768f3a24764" />

## Software and Technologies

- **Programming Language:** Python
- **Computer Vision:** OpenCV
- **Object Detection:** YOLO
- **Depth Sensing:** Intel RealSense SDK
- **Industrial Automation:** Mitsubishi PLC and motion control
- **Robotics:** Delta robot inverse kinematics
- **Palletizing Algorithm:** 3D bin packing and collision checking
- **Monitoring Interface:** Operator interface for system status and control
<img width="801" height="229" alt="image" src="https://github.com/user-attachments/assets/50fccb56-0d4d-42f2-9e92-d0e559997d24" />
<img width="849" height="286" alt="image" src="https://github.com/user-attachments/assets/bf33b9a7-354e-4cab-9440-226340206250" />

## Experimental Results

The system was evaluated under different lighting conditions and during continuous palletizing operation.

| Performance Metric | Experimental Result |
|---|---|
| Average absolute dimension error | 1.28 mm |
| Average relative dimension error | 3.19% |
| Tested lighting conditions | 300–1000 lux |
| Continuous operation test | 1 hour |
| Observed palletizing cycle throughput | Approximately 26–31 pallets/hour |
| Observed product throughput | Approximately 470–620 products/hour |

*Results reflect the tested prototype and experimental conditions. Actual performance depends on object dimensions, robot workspace, cycle time, and operating conditions.*

## Project Demonstration

Add project photos, a system architecture diagram, or a demonstration video here.

- System overview: `docs/architecture.png`
- Vision processing results: `docs/vision-results.png`
- Palletizing demonstration:(https://www.youtube.com/watch?v=zGNEYnBggOM)
<img width="779" height="315" alt="image" src="https://github.com/user-attachments/assets/3e64900d-5cad-4e7b-a25f-509564d07199" />
<img width="641" height="813" alt="image" src="https://github.com/user-attachments/assets/853b9537-c4fd-4b6e-96f5-fa11d0481457" />
<img width="630" height="782" alt="image" src="https://github.com/user-attachments/assets/4f01727b-e1ff-4507-82b8-4232ebdd1365" />

## Project Scope and Limitations

- The system is designed for rectangular boxes within a predefined size range.
- Object measurement accuracy depends on depth data quality, camera calibration, and lighting conditions.
- The palletizing workspace is limited by the Delta robot's reachable workspace.
- The suction end effector is intended for lightweight products with suitable surfaces.
- Pallet layout planning is constrained by collision avoidance, stacking stability, and placement rules.

## Skills Demonstrated

- Python programming
- Computer vision and object detection
- RGB-D image processing
- Camera-to-robot coordinate transformation
- Robot inverse kinematics
- 3D bin packing and pallet layout planning
- PLC communication and industrial motion control
- System integration, testing, and performance evaluation

## Getting Started

The complete setup depends on the available source code, hardware configuration, and installed dependencies.

1. Clone or download this repository.
2. Install the required Python packages.
3. Configure the Intel RealSense camera and vision parameters.
4. Configure PLC communication and robot calibration parameters.
5. Verify the robot workspace and safety conditions before operating the hardware.

Detailed installation and execution instructions will be added based on the final project configuration.

## Disclaimer

This project was developed for academic and educational purposes. Hardware configurations, calibration parameters, and motion commands must be verified for the target system before operation. Always follow appropriate industrial robot safety procedures.
