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


## Project DAVE Integration

### Completed

* Created ROS workspace (`marine_ws`).
* Cloned Project DAVE source into `marine_ws/src/dave`.

### Notes

Project DAVE will be used as the simulation environment for underwater vehicle perception and navigation experiments.

### Next Step

Review installation requirements and launch a baseline underwater simulation.


## Project DAVE Integration

### Repository Inspection

Cloned Project DAVE into:

marine_ws/src/dave

Top-level contents:

* examples
* extras
* gazebo
* legacy
* models
* tools
* urdf

### Observation

Repository structure differs from a typical ROS 2 package layout and requires inspection of installation instructions before building.

### Next Step

Determine compatibility and build process for ROS 2 Lyrical and Gazebo Jetty.


## DAVE Compatibility Investigation

### Discovery

Project DAVE now has an official ROS 2 port targeting:

* ROS 2 Jazzy
* Gazebo Harmonic
* Ubuntu 24.04

The ROS 2 port was developed through Google Summer of Code 2024 and 2025.

### Implication

Current development environment is newer than the documented target platform:

* Ubuntu 26.04
* ROS 2 Lyrical
* Gazebo Jetty

Compatibility must therefore be verified during integration.

### Next Step

Review ROS 2 installation instructions and package dependencies before building.


## DAVE Compatibility Investigation

### Findings

The currently documented ROS 2 version of Project DAVE targets:

* Ubuntu 24.04
* ROS 2 Jazzy
* Gazebo Harmonic

Attempting to run the documented installation procedure on:

* Ubuntu 26.04
* ROS 2 Lyrical
* Gazebo Jetty

may lead to dependency conflicts and broken package installations.

### Decision

Use the officially supported DAVE environment through Docker rather than attempting a native installation on the host system.

### Rationale

The project goal is autonomous underwater inspection and navigation, not simulator maintenance or dependency debugging.
