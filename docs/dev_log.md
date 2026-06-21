# Development Log

## Setup

- Ubuntu 26.04 LTS
- ROS 2 Lyrical
- Gazebo 10.1.1
- Git repository initialized

## Goals

- Install Project DAVE
- Launch underwater vehicle
- Build visual navigation pipeline

## Project Direction

### Candidate Topics Considered

* Visual beacon following
* Docking station approach
* Pipeline inspection
* Subsea structure inspection
* Visual SLAM

### Selected Direction

Develop a vision-based autonomous underwater vehicle capable of detecting, approaching, and inspecting subsea structures within a simulated marine environment.

### Motivation

The project is intended to reflect real-world marine robotics applications such as offshore infrastructure inspection, subsea asset monitoring, and shipwreck exploration.

### Planned Technical Components

* ROS 2 Lyrical
* Gazebo / Project DAVE
* Computer Vision (OpenCV)
* Autonomous Navigation
* Structure-relative positioning


## Project Objective

Develop a simulated autonomous underwater vehicle (AUV) capable of detecting, approaching, and inspecting subsea structures using onboard visual sensing within a ROS 2 and Gazebo-based marine robotics environment.

### Final Demonstration

The AUV will:

1. Detect a subsea structure using camera imagery.
2. Estimate its relative position.
3. Navigate toward the structure autonomously.
4. Maintain a desired inspection distance.
5. Circumnavigate the structure while continuously tracking it.

### Future Extensions

* Multiple-structure inspection missions.
* Autonomous exploration.
* Underwater visual SLAM.
* Shipwreck mapping and inspection.


## Project DAVE Setup

### Current Environment

* Ubuntu 26.04 LTS
* ROS 2 Lyrical
* Gazebo Jetty 10.1.1

### Progress

* ROS workspace created.
* Git repository initialized.
* Began Project DAVE integration.

### Next Goal

Launch the first underwater simulation and verify camera topics are available.
