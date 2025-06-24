# TFG OAR – ROS 2 Unity Project

## Project Documentation – Towards Digital Twins with Unity and ROS 2 for Disaster Robotics

> **Note** This repository builds directly on the work in  
> [TFG_KDN_UnityROS2](https://github.com/Kmdnb/TFG_KDN_UnityROS2/tree/main).  
> Follow *all* setup steps in that project first, then come back here.

---

### Table of Contents
1.  Introduction  
2.  Base‑Project Setup  
3.  Adding the OAR Assets  
4.  New Agents & Features  
5.  Project Execution  
6.  Multimedia  
7.  Credits & Acknowledgements

---

## 1. Introduction

This project is part of an ongoing research line in digital twin technologies for **disaster robotics**, specifically focusing on **Search and Rescue (SAR)** applications. It expands on a previous Unity 3D + ROS 2 simulation of the J8 Rover by introducing new capabilities that bring the system **closer to a real-time digital twin**.

Beyond incorporating new agents such as a multirotor UAV and SAR human units, this project enables the **real-time virtual representation of data received from the physical environment via ROS 2**, enhancing the situational awareness and realism of the simulation.

---

## 2. Base‑Project Setup

Before using this repository:

1. Go to the original project [TFG_KDN_UnityROS2](https://github.com/Kmdnb/TFG_KDN_UnityROS2/tree/main).
2. Follow all steps to correctly install Unity, ROS 2 Humble, ROS‑TCP‑Endpoint, and the Unity–ROS bridge.

Once you have a working version of that base simulation, continue below.

---

## 3. Adding the OAR Assets

### 3.1 Download & Replace Assets

Download this repository and replace the `Assets` folder of the original Unity project with the one provided here.

```bash
# Example command (adjust the path to your project)
cp -r ./TFG-OAR-ROS2-Unity/Assets ./TFG_KDN_UnityROS2/Assets
```

### 3.2 Additional Elements

This folder includes:

- Complete models for the UAV, the J8 rover, and human characters.
- All scripts used for control, simulation, and agent logic.
- Materials and textures for realistic terrain rendering.

### 3.3 Key Scripts Included

The following scripts are included as major innovations in this project:

- `CameraSwitch` – Switch between different Unity cameras using the **C** key.
- `CenitalDroneCamera` – Provides a top-down view of the UAV.
- `DronePoseSubscriber` – Main UAV script that subscribes to GPS data via ROS 2 and moves the drone accordingly.
- `FlyCamera` – Free camera control script.
- `FollowCameraDrone` – Third-person follow view of the UAV.
- `HumanFollower` – Controls SAR agents, showing real-time GPS position and helmet battery percentage.
- `J8TrayectoryFollower` – Main Rover script to show real-time position and odometry from physical sensors.

---

## 4. New Agents & Features

### 4.1 UAV (Multirotor Drone)

- Based on a six-rotor platform inspired by the DJI Matrice 600.
- Controlled via ROS 2 topic with GPS data from a real system.
- Follows waypoints in real-time simulation.

### 4.2 Human SAR Agents

- Human characters representing first responders.
- Each carries a **GPS-enabled helmet** that shares position and battery info with Unity via ROS 2.

---

## 5. Project Execution

To run the full system:

1. Start your ROS 2 environment and launch the nodes that publish GPS and sensor data.
2. Start the ROS-TCP-Endpoint server.
3. Launch the Unity project with the replaced `Assets` folder.
4. ✅ **Verify Unity–ROS 2 communication is working.**

   - In Unity, go to **Robotics → ROS Settings** and configure the IP and port of the ROS 2 machine.
   - Also, in the Hierarchy panel, select the `ROS_Connector` GameObject and in the Inspector configure the same IP and port.

---

## 6. Multimedia

The `multimedia` folder includes:

- Screenshots from the Unity simulation.
- Real photos from field testing with the Rover J8.
- Comparative visuals between simulation and real-world deployment.

---

## 7. Credits & Acknowledgements

- This project was developed as part of an undergraduate thesis in Industrial Electronics Engineering.
- It is built upon the structure and setup of [TFG_KDN_UnityROS2](https://github.com/Kmdnb/TFG_KDN_UnityROS2/tree/main), extending its scope for SAR digital twin research.
