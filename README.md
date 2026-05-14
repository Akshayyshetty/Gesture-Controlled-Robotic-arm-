# Gesture-Controlled-Robotic-arm-
Arduino and Python based robotic arm with gesture/control system
ARM CODE - Arduino code to be uploaded into arm aarduino 
GLOVE CODE - Arduino code to be uploaded into glove 
PYTHON CODE - consists commands to run simulation CV A gesture-controlled robotic hand system that uses MediaPipe for hand tracking, MuJoCo for physics-based simulation, and Arduino for real-time control of robotic movements.

---
🎥 robotic hand demo






## 🧠 Overview
This project enables natural human-computer interaction by capturing hand gestures using a webcam and translating them into robotic finger movements.

It integrates:
	•	MediaPipe for hand tracking
	•	MuJoCo for physics-based simulation
	•	Arduino for real-world hardware control

The system evolves from basic gesture detection to a fully simulated robotic hand, with ongoing integration into a physical robotic hand prototype.

---

🎯 Problem Statement

Traditional robotic systems rely on manual controllers or pre-programmed instructions.
This project aims to develop an intuitive, real-time gesture-based control system that allows users to control robotic hands naturally using human gestures.

---
## ⚙️ Technologies Used
- Python  
- OpenCV  
- MediaPipe (Hand Tracking)  
- NumPy  
- Matplotlib (Early Simulation)  
- MuJoCo (Physics-based Robotic Simulation)  
- Computer Vision  
- Robotics Simulation  

---

## 🔬 Key Features

- 🎯 **Real-time hand gesture tracking**  
- 🤖 **Joint-level robotic finger control**  
- 📐 **Accurate angle calculation using kinematics**  
- 🎮 **Smooth motion using interpolation**  
- 🧊 **Noise reduction (dead zones + filtering)**  
- ⚡ **Real-time FPS and performance monitoring**  
- 🧩 **Modular design (Simulation + Hardware)**  

  ---


 ## 🌍 Applications

This gesture-controlled robotic hand system has potential applications in various real-world domains:

- 🦾 **Prosthetics & Assistive Technology**  
  Can be used to develop advanced prosthetic hands controlled by natural human gestures.

- 🏥 **Medical & Rehabilitation**  
  Useful in physiotherapy and rehabilitation systems for hand movement training and recovery.

- 🏭 **Industrial Robotics**  
  Enables intuitive control of robotic arms for tasks in manufacturing and automation.

- 🎮 **Virtual Reality (VR) & Gaming**  
  Enhances user interaction by enabling gesture-based control in immersive environments.

- 🧠 **Human-Computer Interaction (HCI)**  
  Provides a natural and contactless interface for controlling machines and digital systems.

- 🎓 **Education & Research**  
  Serves as a practical platform for learning robotics, AI, and embedded systems.

- 🪖 **Defense & Hazardous Environments**  
  Can be used for remote operation of robotic systems in dangerous or inaccessible areas.
  CIRCUIT DIAGRAM

FIG 1 : Circuit diagram for robotic arm


FIG 2 : Circuit diagram without Transceiver for robotic arm 



To connect the Transceiver to the circuit in fig 2 below mentioned connections can be used
nRF24L01 to arduino Nano
 GND -> GND
 VCC -> 3.3
 CE -> D7
 CSN -> D8
 SCK ->D13
 MOSI ->D11
 MISO ->D12
 

FIG 3 : Arm Connection

Stage 1: Powering the Servos (The Buck Converter)
Connect your 12V Battery to the IN+ and IN- on the Buck Converter.
Ensure the Buck Converter is tuned to exactly 5 Volts on the output.
Take the Red wires from all 5 servos and connect them to the Buck Converter's OUT+.
Take the Brown/Black wires from all 5 servos and connect them to the Buck Converter's OUT-.
CRITICAL STEP: Connect a jumper wire from the Buck Converter's OUT- to any GND pin on the Arduino Nano. 
Stage 2: Servo Control Signals
Connect the Orange/Yellow signal wires from your 5 servos to the Arduino Nano digital pins:
Thumb Servo -> D5
Index Servo -> D3
Middle Servo -> D6
Ring Servo -> D9
Pinky Servo -> D10
Stage 3: The Wireless Module (nRF24L01)
Connect the 7 pins of the nRF24L01 to the Arduino Nano.
The nRF24L01 must be connected to 3.3V. It will break if connected to 5V
VCC ->3V3 (Arduino 3.3V pin)
GND -> GND (Any Arduino Ground pin)
CE -> D7
CSN -> D8
MOSI -> D11
MISO -> D12
SCK -> D13



FIG 4 : Circuit diagram for glove


FIG 5 : Glove Connection
Stage 1: The nRF24L01 Wireless Module
Connect the 7 pins of the nRF24L01 to the Arduino Nano.
The nRF24L01 must be connected to 3.3V. Do not use 5V
nRF24L01 Pin	Arduino Nano Pin
VCC -> 3V3 (3.3V)
GND ->GND
CE->D7
CSN->	D8
MOSI->D11
MISO->D12
SCK->	D13
Stage 2: The Flex Sensor Circuit (Voltage Divider)
For EVERY finger, build circuit on your breadboard:
Connect Pin 1 of the Flex Sensor to the Arduino's 5V pin.
Connect Pin 2 of the Flex Sensor to an Analog Pin (e.g., A0).
Connect one end of a 10kΩ Resistor to that SAME Analog Pin (A0).
Connect the other end of the 10kΩ Resistor to GND.
Visually, it looks like this:




Analog Pin Mapping:
Thumb Circuit -> A0
Index Circuit -> A1
Middle Circuit -> A2
Ring Circuit -> A3
Pinky Circuit -> A4
Stage 3: Powering the Glove
plug the Glove's Arduino Nano directly into your computer or a standard USB Power Bank using a USB cable.



FIGURE ARE IN THE LINK BEFORE AND FOR MORE INFO CHECK THE DOC BELOW



































LINKS 

Github consist of Arduino code for glove and arm and also python code 
Google drive - https://drive.google.com/drive/folders/1O0cHtS1nPrh4Wb4ZY2ksHELJvQQte4uY?usp=sharing
This consist of images of circuit diagram 
Youtube reference - https://youtu.be/gmz7eOB-tCg?si=ICIN6Kyr2OHmHqep
This consist of video which has done cv control
3D file - Hand and Forarm - InMoov 
This is a Open  source project which consist 3D model and stl file ready to print of different human body parts 
Working videos - https://drive.google.com/drive/folders/1px4CgGKU-tw11mJ0WrqwdxcCiQLmENcb?usp=sharing
DOCS - https://docs.google.com/document/d/1x6gGh7hJj96BO0geRdBvMvd2BCGM97Z4jWJj5-chdZE/edit?usp=sharing


