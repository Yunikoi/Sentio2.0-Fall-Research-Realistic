# 研究计划书 (Research Proposal)

**Name:** 刘沛秋 (Liu Peiqiu)

**Affiliation:** 西安电子科技大学 (Xidian University), Software Engineering

**Prospective Enrollment:** October 2027

**Research Topic:** A Multi-Dimensional Spatial Validation Framework for Outdoor Fall Detection: A Smartphone-Based 5-Sensor Fusion Approach

------

## 1. 研究背景与动机 (Background and Motivation)

Japan has entered a super-aged society, where the safety of elderly individuals during independent outdoor activities is a critical social concern. Falls are a leading cause of injury and mortality among the elderly. While numerous fall detection systems exist, they often face two major challenges:

1. **Low User Compliance:** Many systems require elderly users to wear dedicated sensors (e.g., chest straps or waist-worn IMUs) 24/7. These are often perceived as burdensome or stigmatizing, leading to low adoption.
2. **High False-Alarms in Complex Environments:** Outdoor environments are significantly more "noisy" than indoor settings. Standard IMU-based algorithms frequently trigger false alerts during daily activities such as riding a bus, sudden sitting, or dropping the device.

**HCI Insight:** This research is grounded in a specific behavioral observation: while elderly users rarely carry smartphones inside their homes, they almost universally carry them during outdoor activities for communication, navigation, and emergency purposes. By focusing specifically on an **outdoor-centric, smartphone-based** system, we can maximize reliability where the risk is highest without introducing new, burdensome hardware.

------

## 2. 研究目标 (Research Objectives)

The primary objective of this research is to develop a robust fall detection evidence chain that utilizes the full spatial sensing capabilities of modern smartphones. Specifically, the study aims to:

- Evaluate the synergistic effect of integrating atmospheric (Barometer) and inertial sensors.
- Quantify the reduction in false-positive rates by using a 5-dimensional validation framework compared to traditional 3-axis IMU methods.
- Establish a deterministic "Evidence Chain" of a fall event to ensure high-fidelity alerting.
-
------

## 3. 研究方法 (Methodology)

The proposed system, "Sentio," will implement a **5-Dimensional Sensor Fusion** architecture to analyze the biomechanics of a fall event:

### 3.1 Five-Dimensional Data Integration

The system will synchronize data from five distinct sensor categories:

1. **Barometric Pressure (Altitude):** Captures the instantaneous vertical drop (e.g., from 0.8m pocket height to 0m ground level), serving as the ultimate filter for non-fall activities.
2. **Linear Acceleration (Impact):** Detects the initial weightlessness followed by the high-G impact peak upon contact with the ground.
3. **Rotation Rate (Angular Velocity):** Identifies the chaotic multi-axis tumbling and rotation characteristic of a human fall, distinguishing it from the linear drop of a device.
4. **Gravity Vector (Static Posture):** Monitors the shift of the gravity constant ($9.8 m/s^2$) from the smartphone’s Y-axis (vertical/walking) to the X or Z-axis (horizontal/lying).
5. **Device Orientation (Final State):** Verifies the long-term static orientation post-impact to confirm the user’s inability to regain an upright position.

### 3.2 Preliminary Experimental Design

A 14-day Proof-of-Concept (PoC) will be conducted to validate the framework:

- **Protocol:** Simulated falls (safe squat-to-lie transitions) vs. Daily activities (walking, sitting, descending stairs).
- **Sampling:** Data will be sampled at 50Hz to ensure high-frequency feature capture.
- **Model:** A Random Forest classifier will be trained on the 5-dimensional feature set to evaluate the Accuracy and F1-score of the fused model versus a single-sensor baseline.

------

## 4. 预期成果与意义 (Expected Outcomes)

1. **Technical Proof:** Demonstration that atmospheric pressure (height) and multi-axis rotation are critical for eliminating false alarms in outdoor scenarios.
2. **Architectural Validation:** A validated algorithmic framework that can be integrated into existing smartphone applications without specialized hardware.
3. **Academic Contribution:** Providing a case study on how human behavioral patterns (indoor vs. outdoor phone usage) can inform more effective elderly care technology design.

------

## 5. 研究进度安排 (Research Schedule)

- **2026.04 - 2026.10:** Conduct preliminary experiments, data collection, and baseline model training.
- **2026.11 - 2027.03:** Refine the sensor fusion algorithm; explore more complex outdoor noise scenarios (e.g., public transport, uneven terrain).
- **2027.04 - 2027.09:** Finalize the research proposal and complete prerequisite language/technical preparations for the Master's program.
- **2027.10:** **Enrollment in the Master's Program.** Commence advanced research on robust HCI systems for the aging population.

------

## 6. 参考文献 (References)

