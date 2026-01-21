# 🦾 Practical Control Systems for Robotic Applications (Python)

This repository presents **practical control-system analysis using Python and Jupyter Notebooks**, focused on **real robotic systems** rather than purely theoretical examples.

Each notebook models a real-world robotic subsystem and validates control theory concepts such as **time-domain performance, stability, and delay effects** through simulation.

## ⚙️ Requirements

All dependencies are listed in `requirements.txt`.

Install them using:

```bash
pip install -r requirements.txt
````

Typical libraries used:

* `numpy`
* `matplotlib`
* `control`
* `jupyter`

---

## 📘 Problem 1: Joint Position Control of a Robotic Manipulator

### System Description

A single revolute joint of an industrial robotic arm is actuated by a DC motor.
The motor–joint dynamics are modeled as:


G(s) = {20} / {s(s+5)}


A unity-feedback position control loop is used.

---

### Objectives

* Derive the closed-loop transfer function
* Approximate the system as a **second-order system**
* Compute:

  * Natural frequency (ωₙ)
  * Damping ratio (ζ)
  * Rise time
  * Peak time
  * Percentage overshoot
  * Settling time
* Validate analytical results using **step response simulation**

---

### Practical Relevance

This problem represents:

* Robotic arm joint control
* Pick-and-place manipulators
* CNC machine axes

Excessive overshoot causes:

* Gearbox wear
* Bearing stress
* Reduced positioning accuracy

---

### Notebook

```bash
problem_1_joint_control.ipynb
```

---

## 📘 Problem 2: Stability of a Self-Balancing Mobile Robot

### System Description

A two-wheeled self-balancing robot maintains upright posture using feedback control.
The open-loop transfer function is:

G(s) = {K} / {s(s+1)(s+4)}


---

### Objectives

* Determine the stable range of controller gain **K**
* Analyze stability using pole locations
* Interpret instability in physical terms
* Validate stability numerically

---

### Practical Relevance

This model applies to:

* Self-balancing robots
* Autonomous delivery robots
* Humanoid robot posture control

Instability results in:

* Oscillations
* Motor saturation
* Robot falling

---

### Notebook

```bash
problem_2_balancing_robot.ipynb
```

---

## 📘 Problem 3: Vision-Based Mobile Robot with Time Delay

### System Description

An autonomous mobile robot uses camera-based feedback for navigation.
Image processing and communication introduce a **150 ms time delay**.


G(s) = {K e^{-0.15s}}/{s(s+3)}


---

### Objectives

* Understand why time delay destabilizes robotic systems
* Approximate delay using **first-order Pade approximation**
* Plot and analyze the **root locus**
* Identify stability limits

---

### Practical Relevance

This system models:

* Vision-based navigation
* Remote robot control
* Networked robotic systems (ROS, Wi-Fi, Ethernet)

Time delay is a **common real-world failure mode** in robotics.

---

### Notebook

```bash
problem_3_time_delay_robot.ipynb
```

---

## 🧠 Key Engineering Takeaways

* Time-domain specifications relate directly to **mechanical stress**
* Stability margins determine **robot safety**
* Delay can destabilize even simple control loops
* Simulation is essential before hardware deployment

---

## 🎯 Intended Use

This repository is suitable for:

* Robotics and control systems coursework
* Laboratory assignments
* GitHub portfolio projects
* Technical interviews

---

## 🚀 Future Extensions

* PID controller design and tuning
* Sensor noise and disturbance modeling
* ROS-compatible control blocks
* Automatic report generation from notebooks

---
