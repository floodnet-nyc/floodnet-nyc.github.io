---
layout: default
title: Quality Control
parent: Quality Management
permalink: /quality-management/quality-control/
---

# Quality Control

After the production/assembly stage, quality control (QC) tests are performed on every sensor to validate the data quality. QAP is a quality management procedure followed during the sensor build/assembly process, whereas QC procedures are performed after the complete build procedure and before the deployment.

**Table of Contents:**

* [1.0 General](#10-general)
  + [1.1 Purpose](#11-purpose)
* [2.0 Quality Control](#20-quality-control)
  + [2.1 Sensor Calibration and Data Validation Testing](#21-sensor-calibration-and-data-validation-testing)
    - [Objective](#objective)
    - [Procedure](#procedure)
    - [Calibration](#calibration)
    - [Records](#records)
  + [2.2 Noise floor Testing](#22-noise-floor-testing)
    - [Objective](#objective-1)
    - [Procedure](#procedure-1)
    - [Records](#records-1)
* [References](#references)

## 1.0 General 

### 1.1 Purpose

The purpose of this document is to provide Quality Control (QC) guidelines for 

1. Sensor Calibration and Data Validation Testing

2. Noise Floor Testing

## 2.0 Quality Control

### 2.1 Sensor Calibration and Data Validation Testing

#### Objective

To perform initial calibration and validate sensor data after QAP in laboratory conditions. 

#### Procedure

The mounting bracket lies on a plane higher that the sensor cone. When installed at a known height, the sensor reading is differed by an offset (h_offset) which is equal to the difference between the mount level and the sensor level. 

Therefore when the sensor is mounted at a known height i.e when the mounting bracket is installed at a known height, the sensor reading should lie within the noise floor of the sensor and offset by the value h_offset.

1. Using measuring tape, mount locations are fixed at heights h1, h2, h3, h4 from the surface. 
2. The sensor is mounted at these known heights in order starting from h1 and collects data every 30 seconds for at least 30 minutes, totaling at least 60 measurements.
3. For the next 30 minutes, an object of known height is placed on the surface and measurements are recorded.
4. The object is removed and the sensor is moved onto the next height and the process is repeated until the sensor has been tested at all the heights.

#### Calibration

The data collected from the sensor is used to calibrate and measure the height of the known object. Since measurement of depth is relative to another vertical elevation from a known reference point, this height of the object is a simulation of depth level. 

At every given height, the offset is calculated and transformed into depth levels. The depth shall match the objects height.

#### Records

Calibration offsets and depth averages are recorded for every sensor along with the sensor unique identifiers shall be recorded on this google sheets for reference.

### 2.2 Noise floor Testing

#### Objective

The objective of this test is to perform noise floor testing of the ultrasonic sensor. 

#### Procedure

Data collected from 2.1 is passed through this algorithm to test the noise floor of the sensor.

#### Records

Noise floor for every sensor along with the sensor unique identifiers shall be recorded on this google sheets for reference.

## References

1. [The Spruce, Wire connection problems and solutions](https://www.thespruce.com/wire-connection-problems-and-solutions-1152877)
2. [Adafruit's Tutorial on Good Soldering Practices](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all)
3. [How to Solder: Through-hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all)

