---
layout: default
title: Quality Control
parent: Quality Management
permalink: /quality-management/quality-control/
---

# Quality Control (QC)

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

To perform initial calibration and validation of the sensor depth calculations at different heights in laboratory conditions. 

#### Procedure

1. Using measuring tape, fix mount locations at heights at a known height from the ground. While fixing the mount, using a spirit leveler, make sure the mount is vertical to the mounting surface and horizontal to the ground plane. 
2. Start sensor operation and collect data for at least 120 minutes, with a duty cycle of 60 seconds, totaling at least 120 measurements.
3. After the second step is complete, place an object of known height on the surface, beneath the sensor for the next 120 minutes and record the measurements.
4. Stop the sensor and removing the object.

#### Calibration

To calculate the offset value, take median of all the measurements without the object. To convert distances to depth, invert the distance values and add this calculated offset.

#### Depth Data Validation

Since measurement of depth is relative to another vertical elevation from a known reference point, the height of a known object is used to simulate validation of depth level captured by the sensor.

At a known height, the average of the observed height of the object calculated from the depth values shall be Object's height +- noise floor. 

#### Records

Calibration offsets and depth averages are recorded for every sensor along with the sensor unique identifiers shall be recorded on [this](https://docs.google.com/spreadsheets/d/1FdsjeI8EHIygVHqMOj_p9l_yOaDbCCXwaQY8SxioX9Q/edit?usp=sharing) google sheets for reference.

### 2.2 Noise floor Testing

#### Objective

The objective of this test is to perform noise floor testing of the ultrasonic sensor. 

#### Procedure

Data collected from 2.1 is passed through a [python test script](https://github.com/floodsense/testing/blob/main/scripts/qc_test.py) to test the noise floor of the sensor.

#### Records

Noise floor for every sensor along with the sensor unique identifiers shall be recorded on [this](https://docs.google.com/spreadsheets/d/1FdsjeI8EHIygVHqMOj_p9l_yOaDbCCXwaQY8SxioX9Q/edit?usp=sharing) google sheets for reference.

## References

1. 

