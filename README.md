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
2. Follow all steps to correctly install Unity, ROS 2 Foxy, ROS‑TCP‑Endpoint, and the Unity–ROS bridge.

Once you have a working version of that base simulation, continue below.

---

## 3. Adding the OAR Assets

### 3.1 Download & Replace Assets

Download this repository and replace the `Assets` folder of the original Unity project with the one provided here.

```bash
# Example command (adjust the path to your project)
cp -r ./TFG-OAR-ROS2-Unity/Assets ./TFG_KDN_UnityROS2/Assets
