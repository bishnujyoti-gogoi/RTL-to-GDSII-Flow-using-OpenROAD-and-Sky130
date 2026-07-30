# ⚙️ RTL-to-GDSII ASIC Physical Design Flow using OpenROAD & Sky130

![OpenROAD](https://img.shields.io/badge/OpenROAD-EDA-blue)
![Sky130](https://img.shields.io/badge/Sky130-PDK-green)
![Verilog](https://img.shields.io/badge/Verilog-HDL-orange)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Linux-E95420)
![ASIC](https://img.shields.io/badge/ASIC-Physical%20Design-red)
![License](https://img.shields.io/badge/License-MIT-success)

> Documentation of a complete **RTL-to-GDSII ASIC Physical Design Flow** performed using the **OpenROAD Toolchain** and **SkyWater 130nm (Sky130) Process Design Kit** during the **"VLSI Design Using Open Source Tools"** workshop.

---

# 🖼️ Final Layout

<p align="center">
<img src="Images/final_layout.png" width="900">
</p>

---

# 📖 Project Overview

This repository documents the implementation of a complete **RTL-to-GDSII ASIC Physical Design Flow** using the **OpenROAD** toolchain and **Sky130 Process Design Kit (PDK)**.

The project was completed during the **"VLSI Design Using Open Source Tools"** workshop organized by **Girijananda Chowdhury University** in association with **NiNE Labs, IIT Guwahati**.

A workshop-provided **32-bit synchronous up-counter RTL design** was used as the input design. The primary objective of this project was to understand and execute the complete ASIC physical design workflow—from RTL input to final GDSII layout—using open-source EDA tools.

---

# 🎯 Objectives

- Learn the complete RTL-to-GDSII ASIC implementation flow.
- Understand ASIC physical design using OpenROAD.
- Configure and execute the OpenROAD flow.
- Apply timing constraints.
- Generate timing, area, and power reports.
- Produce the final manufacturable GDSII layout.

---

# 🛠️ Tools & Technologies

- OpenROAD
- SkyWater130 (Sky130) PDK
- Ubuntu Linux
- Verilog HDL (Workshop-provided RTL)
- OpenSTA
- TCL
- ASIC Physical Design Flow

---

# 🔄 ASIC Design Flow

```text
Workshop RTL (Verilog)
        │
        ▼
Configuration
(config.mk)
        │
        ▼
Timing Constraints
(constraint.sdc)
        │
        ▼
Logic Synthesis
        │
        ▼
Floorplanning
        │
        ▼
Placement
        │
        ▼
Clock Tree Synthesis
        │
        ▼
Global Routing
        │
        ▼
Detailed Routing
        │
        ▼
Timing Analysis
        │
        ▼
Power Analysis
        │
        ▼
GDSII Layout
```

---

# 💻 RTL Design

The implementation uses a **32-bit synchronous up-counter** supplied as part of the workshop material.

The workshop focused on understanding the ASIC implementation flow rather than developing the RTL design itself.

<p align="center">
<img src="Images/rtl_design.png" width="700">
</p>

---

# ⚙️ Configuration

The configuration file defines:

- Design Name
- Target Platform (Sky130)
- RTL Path
- Core Utilization
- Placement Density

<p align="center">
<img src="Images/config_mk.png" width="700">
</p>

---

# ⏱️ Timing Constraints

The timing constraint file defines:

- Clock Period (10 ns)
- Input Delay
- Output Delay

<p align="center">
<img src="Images/constraint_sdc.png" width="700">
</p>

---

# 🚀 OpenROAD Execution

The complete ASIC implementation flow was executed through the following stages:

- RTL Import
- Timing Constraint Application
- Logic Synthesis
- Floorplanning
- Placement
- Clock Tree Synthesis (CTS)
- Global Routing
- Detailed Routing
- GDSII Generation

<p align="center">
<img src="Images/execution1.png" width="850">
</p>

<p align="center">
<img src="Images/execution2.png" width="850">
</p>

<p align="center">
<img src="Images/execution3.png" width="850">
</p>

<p align="center">
<img src="Images/execution4.png" width="850">
</p>

---

# 📊 Timing Analysis

## Setup Slack

<p align="center">
<img src="Images/setup_slack.png" width="750">
</p>

---

## Timing Report (Setup Slack, TNS & WNS)

<p align="center">
<img src="Images/timing_report.png" width="750">
</p>

---

# 📏 Design Area & Core Utilization

<p align="center">
<img src="Images/area_report.png" width="750">
</p>

---

# ⏳ Path Delay Analysis

## Maximum Path Delay

<p align="center">
<img src="Images/max_path_delay.png" width="750">
</p>

---

## Minimum Path Delay

<p align="center">
<img src="Images/min_path_delay.png" width="750">
</p>

---

# ⚡ Capacitance Analysis

<p align="center">
<img src="Images/capacitance_report.png" width="750">
</p>

---

# 🔋 Power Analysis

Clock period and power consumption obtained after physical implementation.

<p align="center">
<img src="Images/power_report.png" width="750">
</p>

---

# 🧩 Generated GDSII Layout

Final GDSII layout generated after successful completion of the OpenROAD flow.

<p align="center">
<img src="Images/gds_layout.png" width="850">
</p>

---

# 📂 Repository Structure

```text
RTL-to-GDSII-Flow-using-OpenROAD-and-Sky130
│
├── Images
│   ├── rtl_design.png
│   ├── config_mk.png
│   ├── constraint_sdc.png
│   ├── execution1.png
│   ├── execution2.png
│   ├── execution3.png
│   ├── execution4.png
│   ├── setup_slack.png
│   ├── timing_report.png
│   ├── area_report.png
│   ├── max_path_delay.png
│   ├── min_path_delay.png
│   ├── capacitance_report.png
│   ├── power_report.png
│   ├── gds_layout.png
│   └── final_layout.png
│
├── Report
│   └── workshop_project_report.pdf
│
├── README.md
├── LICENSE
└── .gitignore
```

---

# 📚 Skills Demonstrated

- OpenROAD Toolchain
- ASIC Physical Design Flow
- Sky130 PDK
- Linux-based EDA Workflow
- Floorplanning
- Placement
- Clock Tree Synthesis (CTS)
- Global & Detailed Routing
- Static Timing Analysis (STA)
- Timing Report Interpretation
- Area Analysis
- Power Analysis
- GDSII Layout Generation

---

# 📝 Project Note

This project was completed during the **"VLSI Design Using Open Source Tools"** workshop.

The workshop provided a reference **32-bit synchronous up-counter RTL design**, allowing participants to focus on learning and executing the complete RTL-to-GDSII physical design flow using OpenROAD and the Sky130 PDK.

The emphasis of this project was on understanding ASIC implementation, timing analysis, routing, physical design, and layout generation rather than RTL development.

---

# 🔮 Future Learning Goals

- Learn Verilog HDL in depth
- Develop original RTL designs
- Perform DRC and LVS verification
- Explore OpenLane flow
- Implement larger digital circuits
- Learn low-power ASIC design techniques

---

# 🙏 Acknowledgements

This project was completed as part of the workshop:

**VLSI Design Using Open Source Tools**

Organized by

- Girijananda Chowdhury University
- NiNE Labs, IIT Guwahati

Sponsored by

- Ministry of Electronics & Information Technology (MeitY), Government of India

---

# 👨‍💻 Author

**Bishnujyoti Gogoi**

B.Tech – Electronics & Telecommunication Engineering

Jorhat Institute of Science & Technology

📧 Email: bishnujyotigogoi01@gmail.com

🔗 GitHub: https://github.com/bishnujyoti-gogoi

💼 LinkedIn: https://www.linkedin.com/in/bishnujyoti-gogoi-24b908247/

---

# 📄 Workshop Report

The complete workshop report is available in the **Report** folder.

---

# 📜 License

This project is licensed under the **MIT License**.

⭐ If you found this repository useful, consider giving it a star.
