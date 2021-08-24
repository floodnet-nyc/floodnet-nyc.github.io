---
layout: page
title: Quality Assurance Process
permalink: /quality-assurance-process/
---

# Quality Assurance Process (QAP) - FloodNet

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
    * [Quality Requirements](#quality-requirements)
        * [Hardware](#hardware)
        * [Software](#software)
    * [Quality Assurance Stages with Evaluation](#quality-assurance-stages-with-evaluation)
    * [Quality Assurance Records](#quality-assurance-records)
* [References](#references)

## General

### Purpose

The main objectives of this document are:

- Establish and execute Quality Assurance (QA) measures and procedures to meet high quality sensor standards 
- Provide Quality Control (QC) guidelines for fault identification and rectification, and quality evaluations.

### Scope

This Quality Assurance Process (QAP) applies to all personnel performing sensor development, assembly and validation at FloodNet.

### Roles and Responsibilities

The following table outlines the roles and responsibilities for FloodNet personnel

| FloodNet personnel          | QA Roles                                                     | QA Responsibilities                                          |
| --------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Technical Lead              | 1. QA Manager/Advisor <br />2. Technical Lead                | 1. Manages the project and oversees the big picture<br />2. Uses strong technical skills to help the team solve technical issues |
| Sensor Engineer             | 1. QA Team Test Lead <br />2. QA Validation Specialist <br />3. QA Manual/Automation Test Engineer | 1. Provides Leadership specifically to the test team to support the test teammates and oversee test processes<br /> 2. Participate in validation of the Quality Assurance Process (QAP)<br /> 3. Develop and maintain Manual/Automated test processes |
| Graduate Research Assistant | 1. QA Manual/Automation Test Analyst <br />2. QA Tester      | 1. Develop, maintain and execute Manual/Automated test processes <br />2. Follow strict set of instructions to test or validate the product |

## Training

### Training Needs

### Training Program Implementation

## Quality Assurance Process

The Quality Assurance Process shall be followed staff responsible for performing and verifying work affecting sensor quality. 

### Quality Requirements

The Quality Requirements are classified into two categories: Hardware and Software. QAP process shall be followed on the former first, followed by the later. Software malfunction could be a result of failures in the hardware. Hence, the *QA process shall be reinitiated from the beginning upon identification of bugs in either stages to follow the QAP pipeline.*

#### Hardware

The following is the list of hardware quality requirements:

| Hardware Quality Requirements        | Description                                                  |
| ----------------------------------- | ------------------------------------------------------------ |
| High Quality Electrical Connections | 1. The sensor's hardware must **<u>NOT</u>** have any errors in electrical connections.<br />2. High quality soldering practices |
| Free of Short-Circuits              | 1. The sensor shall have **<u>NO</u>** short-circuits<br />2. The personnel shall check for short-circuits at every stage of the assembly |
| Desired Hardware operation          | 1.  The sensor Hardware shall be functional and tested before moving onto the software stage |
| Waterproofed Sensor                 | 1. All the electrical wire connections lying **<u>inside</u>** as well as **<u>outside</u>** of the sensor shall be waterproofed using heat shrink tubing<br />2. All the external cables and electrical connections outside the sensor shall be waterproofed further either by using liquid electrical tape or silicon<br />3. The housing shall be checked for any defects or potential damage that might cause failure in waterproofing |

#### Software

Stable Sensor Operation

Sensor Accuracy within Tolerance

Good Wireless Connectivity

### Quality Assurance Stages with Evaluation

#### Stage 1: PCB Assembly

PCB fault check

solder battery in using jst

solder switch

turn off the switch

solder screw terminals for US and Solar



solder battery out screw terminal

shorts check

#### Stage 2: MCU Assembly

insert JST 2 pin connecter on the back side of MCU

tan the other ends

cut mcu male headers 

Mount mcu male headers into female headers

insert mcu leaving grounds

connect mcu to Bout

place upside down solder headers onto pcb first

double check if mcu is sitting on the right pins and solder headers onto mcu

solder mcu header pins

MCU pins short check

Screw terminals and MCU connectivity check

end of soldering

#### Stage 3: Battery Assembly

Remove MCU 

insert battery into battery in

turn on the switch

voltage check at bout should be VBat across VB and GND when s/w is on

turn off the switch

#### Evaluation 1: MCU main voltage check

turn on the s/w 

Check electrical connections and monitor voltages

turn off the s/w 

#### Stage 3: Housing Preperation

remove the mounting headers for extra space

drill hole for US
drill hole for antenna dont use step drill - 
drill hole for solar panel



#### Evaluation 2: Housing quality 

check for housing damages

quality of holes 

holes positioning

#### Stage 5: US Assembly

solder wires into US sensor 

check for shorts

stack 2 washers

file the US

Stick e-Tape on the top of MCU

insert US into the housing lid secure using washer and lock nut

#### Stage 7: PCB Mounting

stick PCB using tape

#### Stage 4: Solar Panel Assembly

cut a wire

prepare ends

inert wire through cable gland 

prepare ends and connect to PCB

other end through 3d mount

prepare ends and solder onto the Solar board

screw into the screw terminal through the cable gland

check connectivity solar panel to screw terminals to MCU

#### Evaluation 3: Solar Panel Operation

Flash light 

check voltages 

verify Positives and Negatives 

Check for shorts



#### Stage 6: Antenna Assembly

insert other end of antenna into the housing secure with screws

screw in antenna from the outside 

insert antenna into mcu

#### Evaluation 4: Sensor Operation

flash test firmware check battery voltage and ultrasonic measurement on TTN console

#### Sensor Quality Control Test - 1: Sensor power management test

#### Final steps

close lid 

secure lid with screws 

check - no moving parts 

sensor physical quality check - holes, mounts, securing enclosure, waterproofing

#### Sensor Quality Control Test - 2: Sensor data validation test

#### Sensor Quality Control Test - 3: Solar Power harvesting test

### QA/QC Records



## Troubleshooting. 



## References

[*ER Quality Program Plan*, ES/*ER*/TM-4/R4. (*MMES 1994a*)](https://rais.ornl.gov/documents/tm117.pdf)





