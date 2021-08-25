---
layout: default
title: Quality Assurance Process
parent: Quality Management
permalink: /quality-management/quality-assurance-process/
---

<h1>Quality Assurance Process (QAP)</h1>

This document details the Quality Assurance Process (QAP) at FloodNet. This document details the responsibilities of the Quality Assurance personnel and chain of command for executing the QAP. 

**Table of Contents:**

  * [General](#general)
      * [Purpose](#purpose)
      * [Scope](#scope)
      * [Roles and Responsibilities](#roles-and-responsibilities)
  * [Training](#training)
      * [Training Needs](#training-needs)
      * [Training Program Implementation](#training-program-implementation)
  * [Quality Assurance Process](#quality-assurance-process)
* [References](#references)

<h2>General</h2>

<h3>Purpose</h3>

The main objective of this document is to establish and execute Quality Assurance (QA) measures and procedures to produce high quality sensor standards with consistency.

<h3>Scope</h3>

This Quality Assurance Process (QAP) applies to all personnel performing sensor development, assembly and validation at FloodNet.

<h2>Quality Assurance Process</h2>

The Quality Assurance Process shall be followed staff responsible for performing and verifying work affecting sensor quality. 

### **Stage 1: PCB Assembly**

1. Gather the PCB and a multimeter to check the PCB for any manufacturing defects. To perform the PCB fault check, place one probe on the beginning of the trace and the other on the ending and check for any short circuits like shown in figure 1. Repeat this process for every trace.

2. While placing the PCB upside down, Solder a 2-pin JST connector into the Battery IN like shown in figure 2. 
   <br /><u>Note:</u> All the holes of the screw terminal shall be facing the print on the PCB like shown in figure 2.

3. Now with PCB in the same position, solder the three legs of the slide switch into the ON OFF pins like shown below in figure 3 (There are a total of 5 legs on this components and the legs on the either ends need not to be soldered, i.e. the middle three are the ones that need soldering). The switch does not have polarity but just on and off depending on where the slider lies.

4. Turn the PCB around and make sure the switch is turned of like shown in figure 4.

5. Now with the PCB placed upside down, solder screw terminals for Ultrasonic Sensor and Solar input like shown in the figure 5.

6. Now Solder battery out screw terminals into BAT OUT like shown in figure 6.

7. Using a multimeter check for shorts and connectivity like shown in figure 7. Further quality of the soldering shall be checked at this step and [identify and resolve any soldering errors](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all#common-problems).

### **Stage 2: MCU Assembly**

1. Prepare a 2 Pin JST connector by tanning the other ends. Then, insert the JST 2 pin connecter on the back side of MCU like shown below in figure 8.
2. Now cut the MCU male headers to match the number of through holes on the PCB and the female header pins like shown in the below figure 9.
3. Mount the MCU male headers into female headers like shown in the figure 10 below. 
4. Solder MCU header pins on the top of the MCU while the MCU is securely held by the female header pins on the bottom like shown in figure 11.
5. With the PCB upside down solder the female header pins into the PCB like shown below in figure 12. 
6. Now, connect the 2 ends of the JST connector from the MCU with the BAT OUT into their corresponding terminals VB and G respectively like shown in the figure 13 below.
7. Using a multimeter check for the connectivity between the MCU pins and the screw terminals.

### **Stage 3: Battery Assembly**

1. Remove the MCU from the female header pins and insert a ***fully charged*** 400mAh battery into the BAT IN and secure the battery by using a tape like shown in the figure 14 below.
2. Mount the MCU back onto the headers and make sure the battery is not under pressure or being crushed by the MCU. When the battery and MCU are looking like figure 15, there must be enough space between the MCU and battery.

### **Evaluation 1: Main voltage check**

1. Turn on the switch and check the voltage at BAT OUT. The multimeter reading should be VBat - the battery's voltage level, across VB and GND when the s/w is on like shown below in figure 15.
2. Turn off the switch before proceeding to next steps - figure 16.

### **Stage 4: Housing Preperation**

Instruction on using the step drill, jigs, and other tools {Fill-me-in}

1. Secure the lid of the housing and place a marker right on the center using a ultrasonic-jig. Remove the ultrasonic-jig and drill a hole of diameter {fill-me-in} to accommodate the Ultrasonic sensor like shown in figure 17.
2. Secure the housing with the side that does not have mounting supports facing upwards. Place a marker using the antenna-jig. Remove the antenna-jig and drill a hole of diameter {fill-me-in} to accommodate the antenna like shown in figure 18.
3. Similarly, on the opposite side where there is no mounting support, drill a hole of diameter {fill-me-in} using the pg5-cable-jig to accommodate the solar panel cable like shown in figure 19.

### **Stage 5: US Assembly**

1. Tan both ends of 4 different colored wires and solder one end of the wires onto the Ultrasonic sensor's pins - GND, V+, 5 and 4 respectively like shown in figure 20. 
2. Now twist the cables like shown below in figure 21.
3. Check for connectivity and any [common soldering errors](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all#common-problems).
4. Stack 2 washers that come with the lock nut like shown below in figure 22.
5. Insert US into the housing lid secure it using a lock nut on the inside of the housing lid like shown in figure 23.

### **Stage 7: PCB Mounting**

1. Lift the MCU and screw the PCB onto the mounting headers on the base of the housing. The orientation shall match the one shown in the figure 24.
2. Insert the MCU back into the header pins

### **Stage 4: Solar Panel Assembly**

1. Use a {fill-me-in} wire and cut it to a length of {fill-me-in} like shown in the figure 25.

2. Prepare the ends by tinning them like shown in the figure 26.

3. Place the nut of the PG-7 cable gland inside the housing and insert this prepared end of the wire into the hosuing through a PG-7 cable gland like shown in the figure 27.

4. Screw in the ends into the Solar screw terminals into the respective pins like shown in figure 28.

other end through 3d mount

prepare ends and solder onto the Solar board

screw into the screw terminal through the cable gland

check connectivity solar panel to screw terminals to MCU

### **Evaluation 2: Solar Panel Operation**

Flash light 

check voltages 

verify Positives and Negatives 

Check for shorts

### **Stage 6: Antenna Assembly**

insert other end of antenna into the housing secure with screws

screw in antenna from the outside 

insert antenna into mcu

### **Evaluation 3: Sensor Operation**

flash test firmware check battery voltage and ultrasonic measurement on TTN console

### **Final steps**

close lid 

secure lid with screws 

check - no moving parts 

sensor physical quality check - holes, mounts, securing enclosure, waterproofing

<h2>References</h2>

1. [*ER Quality Program Plan*, ES/*ER*/TM-4/R4. (*MMES 1994a*)](https://rais.ornl.gov/documents/tm117.pdf)




