---

layout: default
title: Quality Assurance Procedure
parent: Quality Management
permalink: /quality-management/quality-assurance-procedure/
---

# Quality Assurance Procedure (QAP)

This document details the Quality Assurance Procedure (QAP) at FloodNet. This document details every stage of the build/assembly procedure to ensure a good sensor build quality.

**Table of contents:**

* [General](#general)
  + [Purpose](#purpose)
* [Quality Assurance Procedure](#quality-assurance-process)
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

The main objective of this document is to establish and execute Quality Assurance Procedure (QAP) to produce high quality sensor builds with consistency.

## Quality Assurance Procedure

The QAP shall be followed by all the personnel responsible for performing and verifying work affecting sensor quality. 

### Stage 1 - Housing Preparation 

Instructions on using the step drill are [here](https://cdn.shopify.com/s/files/1/0012/0350/3168/files/4210T.Manual.20190108.pdf?3927471806556549811)

1. Secure the housing lid using a vice and drill a hole of diameter 1 1/4".

      <img src="/assets/images/IMG_8097.JPG" alt="IMG_8097" style="zoom:18%;" />

   The hole in the lid shall be able accommodate the Ultrasonic sensor.

   <img src="/assets/images/IMG_8101.JPG" alt="IMG_8101" style="zoom:22%;" />

2. Similarly using a step drill and a vice, on the sides with no mounting support, drill a hole of diameter 1/2" on one side and 1/4" on the other side.

   <img src="/assets/images/IMG_8102.JPG" alt="IMG_8102" style="zoom:22.5%;" />

### Stage 2 - PCB Assembly

1. Gather a multimeter and check the PCB for any manufacturing defects. Choose the continuity setting on the multimeter indicated by a small microphone symbol. 

   <img src="/assets/images/IMG_8023.JPG" alt="IMG_8023" style="zoom:18%;" />

   To perform the PCB fault check, place one probe on the beginning of the trace and the other on the ending and check for connectivity as shown in the figure below. Repeat this process for every trace.

   <img src="/assets/images/IMG_8026.jpg" alt="IMG_8026" style="zoom:24%;" />

   <img src="/assets/images/IMG_8025.JPG" alt="IMG_8025" style="zoom:23%;" />

   The both ends of a trace shall have connectivity. Across different traces, continuity shall not be observed unless they share the common pin like GND or V+.

2. While placing the PCB upside down, Solder a 2-pin JST connector into the Battery IN facing towards the center of the board. 
   
   <img src="/assets/images/IMG_8028.JPG" alt="IMG_8028" style="zoom:27%;" />
   
   
   
   <img src="/assets/images/IMG_8027.JPG" alt="IMG_8027" style="zoom:23%;" />
   
3. Now with PCB in the same position, solder the three legs of the slide switch into the ON OFF pins like shown below  (There are a total of 5 legs on this components and the legs on the either ends need not to be soldered, i.e. the middle three are the ones that need soldering). The switch does not have polarity but just on and off depending on where the slider lies.

   <img src="/assets/images/IMG_8103.JPG" alt="IMG_8103" style="zoom:27%;" />

4. Turn the PCB around and make sure the switch is ***turned off***.

5. Now with the PCB placed upside down, solder screw terminals for Ultrasonic Sensor and Solar input like shown below.

   <img src="/assets/images/IMG_8104.JPG" alt="IMG_8104" style="zoom:23%;" />

   <img src="/assets/images/IMG_8105.JPG" alt="IMG_8105" style="zoom:22%;" />

   <u>Note:</u> All the holes of the screw terminal shall be facing the text on the PCB like shown in above figures.

6. Now Solder battery out screw terminals into **BAT OUT** like below.

   <img src="/assets/images/IMG_8106.JPG" alt="IMG_8106" style="zoom:23%;" />

7. Using a multimeter check for shorts and connectivity. Further quality of the soldering shall be checked at this step and [identify and resolve any soldering errors](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all#common-problems).

### Stage 3 - MCU Assembly

1. Now cut the MCU male headers to match the 8-pin female headers as shown in the below figure.

   <img src="/assets/images/IMG_8108.JPG" alt="IMG_8108" style="zoom:18%;" />

2. Insert these male headers into female headers and place the MCU's first eight pins, both sides on top of these male headers. Solder header pins while the MCU is securely held by the female header pins, as shown in the figure below.

   <img src="/assets/images/IMG_8109.JPG" alt="IMG_8109" style="zoom:23%;" />

3. With the PCB upside down solder the female header pins into the PCB like shown below. Make sure PCB is facing the right direction and inserted into the correct pins. 

   <img src="/assets/images/IMG_8111.JPG" alt="IMG_8111" style="zoom:25%;" />

   <img src="/assets/images/IMG_8113.JPG" alt="IMG_8113" style="zoom:23%;" />

4. Using a multimeter check for the connectivity between the MCU pins and the screw terminals.

### Stage 4 - Battery Assembly

1. With the switch turned ***off***, remove the MCU from the female header pins and insert a ***fully charged*** 400 mAh battery into the **BAT IN**.

   <img src="/assets/images/IMG_8114.JPG" alt="IMG_8114" style="zoom:23%;" />

2. Prepare a 2 Pin JST connector by tanning the other ends. Insert the connecter on the back side of MCU as shown below.

   <img src="/assets/images/IMG_8107.JPG" alt="IMG_8107" style="zoom:40%;" />

3. Connect the JST connector with **BAT OUT** into their corresponding **VB** and **G**, respectively, as shown below.

   <img src="/assets/images/IMG_8115.JPG" alt="IMG_8115" style="zoom:13%;" />

4. Mount the MCU back onto the headers and make sure the battery is not under any pressure or being crushed by the MCU. When done correctly battery should be only held by the JST connector and sits comfortably under the MCU.

   <img src="/assets/images/IMG_8119.JPG" alt="IMG_8119" style="zoom:22%;" />

### Evaluation 1 - Main voltage check

1. Turn on the switch and check the voltage at BAT OUT. The multimeter reading should be **VBat** - the battery's voltage level, across **VB** and **GND** when the s/w is on.
2. ***Turn off*** the switch before proceeding to next steps when the evaluation has been successfully completed.

### Stage 5 - Ultrasonic Sensor Assembly

1. Tan both ends of 4 different colored wires and solder one end of the wires onto the Ultrasonic sensor's pins - GND, V+, 5 and 4.

2. Carefully, without applying too much pressure on the solder joints, twist them like shown.

   <img src="/assets/images/IMG_8120.JPG" alt="IMG_8120" style="zoom:22%;" />

3. Check for connectivity and any [common soldering errors](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all#common-problems).

4. Stack 2 washers that come with the lock nut like shown below.

   <img src="/assets/images/IMG_8121.JPG" alt="IMG_8121" style="zoom:16%;" />

5. Insert US into the housing lid secure it using a lock nut on the inside of the housing lid.

   <img src="/assets/images/IMG_8122.JPG" alt="IMG_8122" style="zoom:14%;" />

   <img src="/assets/images/IMG_8124.JPG" alt="IMG_8124" style="zoom:14%;" />

6. Connect V+ of ultrasonic sensor to the VE of PCB.

   Connect GND of ultrasonic sensor to the G of PCB.

   Connect pin 4 of ultrasonic sensor to the G5 of PCB.

   Connect pin 5 of ultrasonic sensor to the RX of PCB.

   <img src="/assets/images/IMG_8126.JPG" alt="IMG_8126" style="zoom:18%;" />

### Stage 6 - PCB Mounting and Antenna Assembly

1. Using a plier, cut the legs on the bottom of the soldered PCB to save some room.

2. Connect the MHF4 female to the MCU and secure SMA female end into the housing using a nut.

   <img src="/assets/images/IMG_8128.JPG" alt="IMG_8128" style="zoom:18%;" />

3. Insert the PCB into the housing by sliding it under the antenna like shown.

   <img src="/assets/images/IMG_8129.JPG" alt="IMG_8129" style="zoom:18%;" />

4. Lift the MCU and screw the PCB onto the mounting headers on the base of the housing. The orientation shall match the housing holes: 1/2" hole shall be facing the solar input.

   <img src="/assets/images/IMG_8134.JPG" alt="IMG_8134" style="zoom:18%;" />

5. Insert the MCU back into the header pins and screw the other end of the PCB into the housing.

   <img src="/assets/images/IMG_8135.JPG" alt="IMG_8135" style="zoom:18%;" />

6. Screw in a male LoRa antenna (should support 915 MHz) onto the SMA female connector.

   <img src="/assets/images/IMG_8138.JPG" alt="IMG_8138" style="zoom:18%;" />

### Stage 7 - Solar Panel Assembly

1. Cut an alarm cable or 2 conductor wire to a length of 30cm or 12 inches. Prepare the ends by tinning them.

   *<u>Note:</u> Adjust the length so that cable can reach from the sensor to the panel based on the chosen mount.*

   <img src="/assets/images/IMG_8139.JPG" alt="IMG_8139" style="zoom:18%;" />

2. Stick one side of the gasket onto the 3D-mount and run one end of the solar cable through the 3D-mount like shown.

   <img src="/assets/images/IMG_8141.JPG" alt="IMG_8141" style="zoom:18%;" />

3. Solder the panel to this end that runs through the 3D-mount and gasket. 

   <img src="/assets/images/IMG_8142.JPG" alt="IMG_8142" style="zoom:18%;" />

   <img src="/assets/images/solar-solder.jpg" alt="solar-solder" style="zoom:18%;" />

4. Seal the panel using the gasket.

   <img src="/assets/images/IMG_8147.JPG" alt="IMG_8147" style="zoom:14%;" />

5. Place the nut of the PG-7 cable gland inside the housing and insert the other prepared end of the solar cable into the housing through a PG-7 cable gland.

   <img src="/assets/images/IMG_8150.JPG" alt="IMG_8150" style="zoom:18%;" />

6. Screw the open ends of the solar cable into the screw terminal SOLAR. Secure the cable gland.

   <img src="/assets/images/IMG_8153.JPG" alt="IMG_8153" style="zoom:18%;" />

   <img src="/assets/images/IMG_8155.JPG" alt="IMG_8155" style="zoom:18%;" />

### Evaluation 2 - Solar Panel Operation

1. Check for connectivity between both the ends of the solar cable. Also check for shorts between the **VS** and **GND**.
2. Flash light onto the solar panel and check voltages on the screw terminals using a multimeter. When a phone falshlight is flashed upon the panel, it should read atleast 3 Volts. 

2. Now with the light is being flashed onto the panel, verify the **VS** is the ***positive*** terminal. If not, the solar panel has been soldered in reverse and shall be re-soldered so that a positive voltage is seen across **VS** and **GND**.

### Evaluation 3 - Sensor Operation

1. Flash the test firmware and check the battery voltage and ultrasonic measurements on TTN console. The battery voltage shall be between 3.7 Volts and 4.2 Volts. Since we would be using a fully charged battery, it should read voltage greater than 4 Volts. The distance reading on the TTN console shall be greater than or equal to 300 and less than or equal to the maximum range of the sensor model. The 5-meter model range is 300mm to 5000mm and the 10-meter model range is 300mm to 10000mm.

### Final steps

1. Close the lid and make sure the ultrasonic sensor wires goes into the space safely to avoid them being in the way. 
2. Now secure the lid with screws 
3. The sensor shall feel robust and when invereted there shall be no moving parts.
4. Inspect the sensor mechanical quality of the following: holes, mounts, securing enclosure, waterproofing. 

## References

1. [*ER Quality Program Plan*, ES/*ER*/TM-4/R4. (*MMES 1994a*)](https://rais.ornl.gov/documents/tm117.pdf)
2. [The Spruce, Wire connection problems and solutions](https://www.thespruce.com/wire-connection-problems-and-solutions-1152877)
3. [Adafruit's Tutorial on Good Soldering Practices](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all)
4. [How to Solder: Through-hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all)
