---
title: "Automated Hemorrhage Resuscitation"
excerpt: "A physiological closed-loop system for automated hemorrhage care."
header:
  image: /assets/img/hemorrhage_website.png
  teaser: /assets/img/hemorrhage_electronics.png
gallery:
  - image_path: assets/img/hemorrhage_box.png
  - image_path: assets/img/pulsatile_pump.png
  - image_path: assets/img/hemorrhage_electronics_square.png
   
---

## Project Overview

Hemorrhage is a leading cause of preventable death in trauma care, particularly in austere environments where access to advanced medical personnel and hospital care may be delayed. This project involved the development of a physiological closed-loop system for automated fluid resuscitation.

The system is intended to support soldiers and other trauma patients during the period between injury and arrival at a hospital. It continuously evaluates patient physiology, classifies the severity of hemorrhagic shock, and delivers an appropriate fluid response through automated pumps and valves.

## Design Purpose and Features

The system was designed to provide standardized and responsive hemorrhage care in environments with limited personnel, supplies, and monitoring capabilities.

Key features include:
- **Multi-parameter assessment:** The system extracts five physiological variables:
  - Systolic blood pressure (SBP)
  - Diastolic blood pressure (DBP)
  - Mean arterial pressure (MAP)
  - Pulse pressure (PP)
  - Heart rate (HR)
- **Closed-loop control:** Physiological feedback is used to determine the appropriate fluid-resuscitation response.
- **Automated fluid delivery:** Solenoid valves and peristaltic pumps control the delivery of crystalloid solution, packed red blood cells, and vasopressor medication.
- **Compact and modular architecture:** The system is designed to be transported and operated in resource-limited environments.
- **Real-time assessment:** Patient state is reassessed at regular intervals using recent physiological data.

## System Architecture

The system integrates **LabChart, MATLAB, and Arduino** software and hardware.

LabChart collects physiological signals, while MATLAB processes the data and extracts the relevant cardiovascular variables. The system then classifies the patient’s hemorrhagic shock state and sends a command to the Arduino microcontroller. The Arduino controls the solenoid valves and peristaltic pumps responsible for fluid delivery.

The control process follows this general sequence:

1. Acquire arterial pressure data through a single arterial line.
2. Filter the pressure signal and calculate SBP, DBP, MAP, and PP.
3. Estimate heart rate using frequency-based signal processing.
4. Classify the patient’s hemorrhagic shock state.
5. Select a fluid-delivery command.
6. Activate the appropriate valves and pumps.
7. Monitor the system for fluid-line bubbles and signal interruptions.

## Off-the-Shelf Parts

| Component | Quantity | Function |
|---|---:|---|
| Ultrasonic bubble sensors | 3 | Detect bubbles in the fluid lines |
| Solenoid valves | 3 | Control fluid-line opening and closing |
| Peristaltic pumps | 2 | Deliver fluids at controlled rates |
| Arterial pressure transducer | 1 | Measures arterial pressure |
| Arduino microcontroller | 1 | Controls valves, pumps, and sensor feedback |
| Relay | 1 | Interfaces the Arduino with pumps and valves |
| Busbar | 2 | Distribute power among electronic components |
| 12V power supply | 1 | Powers the sensors and valves |
| 24V power supply | 1 | Powers the pumps |
| IV tubing and connectors | 10 ft | Transfer fluid through the system |
| Fluid bags | 3 | Store crystalloid, blood, and vasopressor solutions |
| Electrical wiring | 30 ft | Connect system components |
| M5 screws | 8 | Secure electronics enclosure to the IV pole |
| IV pole | 1 | Provides portable base for electronics and fluids |

## 3D-Printed Components

| Printed Component | Quantity | Function |
|---|---:|---|
| Electronics enclosure body | 1 | Organizes and holds the control electronics |
| Electronics enclosure lid | 1 | Protects the control electronics by screwing into the enclosure body |
| Electronics enclosure bracket | 1 | Secures the enclosure body to the IV pole |

## Final Design

The final system combines a monitoring platform, physiological data-processing pipeline, automated fluid-delivery system, and safety-monitoring components. The electronics enclosure houses the control hardware, while the pump and valve assemblies regulate the delivery of multiple fluids.

![Automated hemorrhage-resuscitation system](/assets/img/hemorrhage_setup.png)

## Arduino Code

The Arduino code used to control the pumps, solenoid valves, and sensor feedback is [available on GitHub](https://gist.github.com/colleenmburke/d0f41d8d280c0e27e17f4a7c7ab6ebcd).

## Interactive Fusion 360 Model

The interactive Fusion 360 model of the assembly is embedded below:

<iframe src="https://a360.co/4i2Bq0g"
        width="800"
        height="600"
        allowfullscreen="true"
        webkitallowfullscreen="true"
        mozallowfullscreen="true"
        frameborder="0">
</iframe>

## How to Operate the System

1. Connect the arterial pressure transducer to the patient’s arterial line or benchtop setup.
2. Connect the fluid bags to their designated tubing lines and confirm that the blood, crystalloid, and vasopressor lines are connected correctly.
3. Verify that the peristaltic pumps, solenoid valves, and ultrasonic bubble sensors are connected to the control system.
4. Plug in the 12V and 24V power supplies.
5. Start LabChart and begin acquiring the arterial pressure signal.
6. Start the MATLAB processing and control script.
7. Confirm that the Arduino is receiving commands and communicating with the pumps, valves, and sensors.
8. Allow the system to classify the patient’s physiological state.
9. The system will automatically select and deliver the appropriate fluid response.
10. Monitor the system for bubble detection, signal loss, or other fault conditions.

This project is a research prototype and is not intended for clinical use without additional validation, regulatory review, and safety testing.


{% include gallery caption="Automated Hemorrhage Resuscitation Gallery" %}
