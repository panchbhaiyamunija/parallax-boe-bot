# Parallax Boe-Bot: Corner Escaping & Autonomous Navigation

Autonomous obstacle-avoidance robot built on the Parallax Boe-Bot and BS2 microcontroller using PBASIC. This project implements corner-escape routines by tracking alternating whisker sensor hits to prevent the robot from getting trapped in corner loops.

## Video Demonstration
[Watch the Boe-Bot Autonomous Navigation Demo on LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:7524893705414115328/)

## Hardware & Tech Stack
- **Microcontroller:** Parallax BASIC Stamp 2 (BS2) / Board of Education
- **Language:** PBASIC 2.5
- **Sensors:** Dual tactile whiskers (P5 & P7)
- **Actuation:** Continuous-rotation servos (P12 & P13)

## Code Architecture
- `EscapingCorners.bs2`: Tracks consecutive alternating contact events using state memory (`old5`, `old7`). If trapped in a corner loop (4 consecutive alternate hits), it executes a 180-degree turn sequence.
