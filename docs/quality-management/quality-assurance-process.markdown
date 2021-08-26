---
layout: default
title: Quality Assurance Process
parent: Quality Management
permalink: /quality-management/quality-assurance-process/
---

# Quality Assurance Process (QAP)

This document details the Quality Assurance Process (QAP) at FloodNet. This document details the responsibilities of the Quality Assurance personnel and chain of command for executing the QAP. 

**Table of contents:**

* [General](#general)
  + [Purpose](#purpose)
* [Quality Assurance Process](#quality-assurance-process)
  + [Stage 1 - PCB Assembly](#stage-1---pcb-assembly)
  + [Stage 2 - MCU Assembly](#stage-2---mcu-assembly)
  + [Stage 3 - Battery Assembly](#stage-3---battery-assembly)
  + [Evaluation 1 - Main voltage check](#evaluation-1---main-voltage-check)
  + [Stage 4 - Housing Preperation](#stage-4---housing-preperation)
  + [Stage 5 - Ultrasonic Sensor Assembly](#stage-5---ultrasonic-sensor-assembly)
  + [Stage 6 - PCB Mounting](#stage-6---pcb-mounting)
  + [Stage 7 - Solar Panel Assembly](#stage-7---solar-panel-assembly)
  + [Evaluation 2 - Solar Panel Operation](#evaluation-2---solar-panel-operation)
  + [Stage 8 - Antenna Assembly](#stage-8---antenna-assembly)
  + [Evaluation 3 - Sensor Operation](#evaluation-3---sensor-operation)
  + [Final steps](#final-steps)
* [References](#references)

## General

### Purpose

The main objective of this document is to establish and execute Quality Assurance (QA) measures and procedures to produce high quality sensor standards with consistency.

## Quality Assurance Process

The Quality Assurance Process shall be followed staff responsible for performing and verifying work affecting sensor quality. 

### Stage 1 - PCB Assembly

1. Gather the PCB and a multimeter to check the PCB for any manufacturing defects. To perform the PCB fault check, place one probe on the beginning of the trace and the other on the ending and check for any short circuits like shown in figure 1. Repeat this process for every trace.

2. While placing the PCB upside down, Solder a 2-pin JST connector into the Battery IN like shown in figure 2. 
   <br /><u>Note:</u> All the holes of the screw terminal shall be facing the print on the PCB like shown in figure 2.

3. Now with PCB in the same position, solder the three legs of the slide switch into the ON OFF pins like shown below in figure 3 (There are a total of 5 legs on this components and the legs on the either ends need not to be soldered, i.e. the middle three are the ones that need soldering). The switch does not have polarity but just on and off depending on where the slider lies.

4. Turn the PCB around and make sure the switch is turned of like shown in figure 4.

5. Now with the PCB placed upside down, solder screw terminals for Ultrasonic Sensor and Solar input like shown in the figure 5.

6. Now Solder battery out screw terminals into BAT OUT like shown in figure 6.

7. Using a multimeter check for shorts and connectivity like shown in figure 7. Further quality of the soldering shall be checked at this step and [identify and resolve any soldering errors](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all#common-problems).

### Stage 2 - MCU Assembly

1. Prepare a 2 Pin JST connector by tanning the other ends. Then, insert the JST 2 pin connecter on the back side of MCU like shown below in figure 8.
2. Now cut the MCU male headers to match the number of through holes on the PCB and the female header pins like shown in the below figure 9.
3. Mount the MCU male headers into female headers like shown in the figure 10 below. 
4. Solder MCU header pins on the top of the MCU while the MCU is securely held by the female header pins on the bottom like shown in figure 11.
5. With the PCB upside down solder the female header pins into the PCB like shown below in figure 12. 
6. Now, connect the 2 ends of the JST connector from the MCU with the BAT OUT into their corresponding terminals VB and G respectively like shown in the figure 13 below.
7. Using a multimeter check for the connectivity between the MCU pins and the screw terminals.

### Stage 3 - Battery Assembly

1. Remove the MCU from the female header pins and insert a ***fully charged*** 400mAh battery into the BAT IN and secure the battery by using a tape like shown in the figure 14 below.
2. Mount the MCU back onto the headers and make sure the battery is not under pressure or being crushed by the MCU. When the battery and MCU are looking like figure 15, there must be enough space between the MCU and battery.

### Evaluation 1 - Main voltage check

1. Turn on the switch and check the voltage at BAT OUT. The multimeter reading should be VBat - the battery's voltage level, across VB and GND when the s/w is on like shown below in figure 15.
2. Turn off the switch before proceeding to next steps - figure 16.

### Stage 4 - Housing Preperation

Instruction on using the step drill, jigs, and other tools {Fill-me-in}

1. Secure the lid of the housing and place a marker right on the center using a ultrasonic-jig. Remove the ultrasonic-jig and drill a hole of diameter {fill-me-in} to accommodate the Ultrasonic sensor like shown in figure 17.
2. Secure the housing with the side that does not have mounting supports facing upwards. Place a marker using the antenna-jig. Remove the antenna-jig and drill a hole of diameter {fill-me-in} to accommodate the antenna like shown in figure 18.
3. Similarly, on the opposite side where there is no mounting support, drill a hole of diameter {fill-me-in} using the pg5-cable-jig to accommodate the solar panel cable like shown in figure 19.

### Stage 5 - Ultrasonic Sensor Assembly

1. Tan both ends of 4 different colored wires and solder one end of the wires onto the Ultrasonic sensor's pins - GND, V+, 5 and 4 respectively like shown in figure 20. 
2. Now twist the cables like shown below in figure 21.
3. Check for connectivity and any [common soldering errors](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all#common-problems).
4. Stack 2 washers that come with the lock nut like shown below in figure 22.
5. Insert US into the housing lid secure it using a lock nut on the inside of the housing lid like shown in figure 23.

### Stage 6 - PCB Mounting

1. Lift the MCU and screw the PCB onto the mounting headers on the base of the housing. The orientation shall match the one shown in the figure 24.
2. Insert the MCU back into the header pins

### Stage 7 - Solar Panel Assembly

1. Use a {fill-me-in} wire and cut it to a length of {fill-me-in} like shown in the figure 25.

2. Prepare the ends by tinning them like shown in the figure 26.

3. Place the nut of the PG-7 cable gland inside the housing and insert this prepared end of the wire into the hosuing through a PG-7 cable gland like shown in the figure 27.

4. Screw in the ends into the Solar screw terminals into the respective pins like shown in figure 28.

5. Stick one side of the gasket onto the 3d mount and run the other end of the solar cable through the 3d mount like shown in figure 29. Leave enough space for soldering the solar panel.

6. Now, prepare the ends by stripping the wires and tinning them and solder the ends onto the Solar board like shown in figure 30.
7. Screw the open ends of the solar cable into the screw terminal SOLAR through the cable gland and check connectivity between the solar panel and screw terminals like shown in figure 31.

### Evaluation 2 - Solar Panel Operation

1. Check for connectivity between both the ends of the solar cable. Also check for shorts between the VS and GND {figure 32}
2. Flash light onto the solar panel and check voltages on the screw terminals using a multimeter like shown below. When a phone falshlight is  flashed upon the panel, it should read atleast 3 Volts. {figure 33}

2. Now with the light is being flashed onto the panel, verify the VS is the positive terminal. If not, the solar panel has been soldered in reverse and shall be re-soldered so that a positive voltage is seen on the VS. {figure 34}

### Stage 8 - Antenna Assembly

1. Stack a star washer and lock washer and insert the end of the antenna with threading into the housing from the inside like shown in the figure 35
2. Secure it using a screw from the outside like shown in figure 36
3. Insert the ulf connector of the antenna onto the MCU like shown in figure 37.
4. Screw in the LoRa Antenna from the outside like shown in the figure 38. The antenna should feel tight after screwing onto the threading. If not, try washers of different size.

### Evaluation 3 - Sensor Operation

1. Flash the test firmware and check the battery voltage and ultrasonic measurements on TTN console. The battery voltage shall be between 3.7 Volts and 4.2 Volts. Since we would be using a fully charged battery, it should read voltage greater than 4 Volts. The distance reading on the TTN console shall be greater than or equal to 300 and less than or equal to the maximum range of the sensor model. The 5-meter model range is 300mm to 5000mm and the 10-meter model range is 300mm to 10000mm. {figure 39}

### Final steps

1. Close the lid and make sure the ultrasonic sensor wires goes to the {} to avoid the wires being in the way. {figure 40}

2. Now secure the lid with screws {figure 41}

3. The sensor shall feel robust and when invereted there shall be no moving parts.

4. Inspect the sensor mechanical quality of the following: holes, mounts, securing enclosure, waterproofing. {figure 42}
5. Remove the tape on the gasket and install the solar panel onto the 3D mount {figure 43}

## References

1. [*ER Quality Program Plan*, ES/*ER*/TM-4/R4. (*MMES 1994a*)](https://rais.ornl.gov/documents/tm117.pdf)
