# A structured, Colab-based learning project for studying Modern C++ through robotics and Visual SLAM.

This repository represents a stage of my personal learning journey, developed through a structured and iterative process with guidance and discussion with ChatGPT. The topics, exercises, implementation questions, and progression were selected and refined according to my learning needs and research goals.

The project connects Modern C++ programming concepts with the mathematical, algorithmic, and software structures encountered in Visual SLAM.

---

## ☁️ Colab-first approach

The project is intentionally organized around Google Colab to reduce the software and hardware barriers commonly associated with robotics development and make the learning and experimentation process accessible through a web browser.

---

## 📚 Contents

### Chapter 1 — Modern C++ Foundations

The first chapter focuses on the C++ concepts that are particularly important when working with robotics and SLAM codebases.

* Pass by Value / Reference
* Pointers
* Dereferencing
* Heap Memory
* Structs
* Constructors / Destructors
* Header Files
* `typedef` / `using`
* Smart Pointers
* `const`
* Templates
* STL
* `argv` / Argument Vector
* Dependency Injection
* Debugging
* CMake

The emphasis is on understanding not only **what** these features do, but also **why they appear so frequently in robotics software**.

---

### Chapter 2 — SLAM Mathematics

This chapter introduces the mathematical foundations required to understand the main components of a Visual SLAM system.

#### Camera Model & Projection

Understanding how 3D points are projected into the image plane and how camera parameters affect this projection.

#### Triangulation

Recovering 3D structure from multiple observations of the same feature.

#### Perspective-n-Point (PnP)

Estimating camera pose from known 3D points and their corresponding 2D image observations.

#### Lie Groups — Quick Review

A practical review of:

* SO(3)
* SE(3)
* Rotation and rigid-body transformations
* Lie algebra
* Exponential and logarithmic maps

The focus is on the concepts needed to understand pose representation and optimization in Visual SLAM.

---

# Chapter 3 — Optimization

This chapter moves from the geometric foundations of SLAM toward optimization-based estimation.

### Nonlinear Optimization

Introduction to the concepts behind nonlinear least-squares optimization and their role in parameter estimation.

### g2o — Graph Optimization

Understanding how SLAM problems can be represented as graphs consisting of:

* Vertices
* Edges
* States
* Measurements
* Error functions
* Jacobians
* Optimization

### Bundle Adjustment (BA)

Understanding the joint optimization of camera poses and 3D landmarks using reprojection errors.

### Backend

Exploring the role of the backend in a Visual SLAM system, including:

* Maintaining the optimization problem
* Adding keyframes
* Adding landmarks
* Constructing optimization edges
* Running nonlinear optimization
* Updating the map

### Pose Graph

Understanding how camera/keyframe poses can be represented as a graph and optimized using relative pose constraints.

### Loop Closure

Studying how recognizing a previously visited location can provide additional constraints and reduce accumulated drift.

### Our Complete SLAM Map

Connecting the individual concepts into a complete high-level view of a Visual SLAM pipeline, from image observations and feature extraction to estimation, mapping, optimization, and loop closure.

---

# Chapter 4 — State Estimation

This chapter introduces probabilistic estimation methods that form an important foundation for robotics and sensor fusion.

```text
Probability & Gaussian
        │
        ▼
Bayesian Estimation
        │
        ▼
Kalman Filter
        │
        ▼
Extended Kalman Filter
        │
        ▼
Sensor Fusion
```

Topics include:

* Probability and Gaussian distributions
* Bayesian estimation
* Kalman filtering
* Extended Kalman filtering
* Sensor fusion

The goal is to understand how uncertain measurements and system models can be combined to estimate the hidden state of a robotic system.

---

## 🎯 Learning Goals

This repository aims to develop the ability to:

* Read modern C++ robotics code with confidence.
* Understand pointers, references, memory, and smart pointers in real SLAM code.
* Understand how C++ software is organized using headers, classes, templates, STL, and CMake.
* Connect mathematical concepts to their implementation in C++.
* Understand the geometry behind Visual SLAM.
* Understand graph-based optimization and Bundle Adjustment.
* Understand the role of state estimation and sensor fusion in robotics.
* Follow a complete Visual SLAM pipeline from perception to optimization.
* Develop the foundations required to work with larger robotics codebases such as **g2o, Sophus, OpenCV, and SLAM frameworks**.

---

## 🔗 From C++ to SLAM

One of the main ideas behind this repository is that learning C++ in isolation is not enough for robotics.

For example:

```text
C++ Foundations
      │
      ├── pointers / references
      ├── classes / constructors
      ├── smart pointers
      ├── templates / STL
      ├── debugging
      └── CMake
              │
              ▼
      Robotics Software
              │
              ├── Camera
              ├── Frame
              ├── MapPoint
              ├── Feature
              └── Backend
                      │
                      ▼
                 Visual SLAM
                      │
              ├── Projection
              ├── Triangulation
              ├── PnP
              ├── SE(3)
              ├── Optimization
              ├── Bundle Adjustment
              └── Loop Closure
```

The purpose is therefore to learn the programming concepts **in the context in which they are actually used**.

---

## 🛠️ Technologies & Tools

The material is developed around technologies commonly encountered in robotics and Visual SLAM, including:

* **C++**
* **Python**
* **OpenCV**
* **Eigen**
* **Sophus**
* **g2o**
* **CMake**
* **Google Colab**
* **Linux / Ubuntu**
* **Git / GitHub**

---

## 📖 Learning Approach

The notes follow a concept-first approach:

> **Understand → Connect to robotics → Implement → Debug → Apply to SLAM**

Rather than memorizing isolated C++ syntax or mathematical formulas, the goal is to understand how individual concepts fit together inside a real robotic system.

The repository is therefore both:

1. a personal learning record, and
2. a structured reference for revisiting C++ and Visual SLAM concepts.

---

## 🚧 Status

This repository is an **ongoing learning and implementation project**.

The material currently covers the foundations of Modern C++, Visual SLAM geometry, optimization, and state estimation. Additional examples, implementation details, experiments, and debugging notes may be added as the Visual SLAM study progresses.

---

## 👤 Author

**Fatemeh Nemati**

M.Sc. in Artificial Intelligence & Robotics
M.Sc. in Mechanical Engineering

Research interests include:

* Visual SLAM
* State Estimation
* Computer Vision
* Multi-Object Tracking
* Multi-Camera Perception
* Autonomous Robotics
* Multi-Robot Systems
* Robot Perception

GitHub: [FatemehNMT](https://github.com/FatemehNMT)

---

