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

1. Using measuring tape, fix mount locations at heights h1, h2, h3, h4 from the surface. 
2. Miount the sensor at these known heights in order starting from h1 and collect data every 30 seconds for at least 30 minutes, totaling at least 60 measurements.
3. Place a known object on the surface beneath the sensor for the next 30 minutes and record the measurements.
4. Remove the object and move the sensor onto the next height and repeat the process until the sensor has been tested and recorded at all the heights h1, h2, h3 and h4.

#### Calibration

Calculate offset value for every heights by taking median of these measurements. Invert the distance values and add this calculated offset values to obtain depth values.

#### Data Validation

Since measurement of depth is relative to another vertical elevation from a known reference point, the height of a known object is used to simulate validation of depth level captured by the sensor.

At every given test height h1, h2, h3, and h4, the average of the observed height of the object calculated from the depth values shall be Real Object's height +- noise floor. 

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

1. 
