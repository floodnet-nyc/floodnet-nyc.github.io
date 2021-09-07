---
layout: default
title: Quality Control
parent: Quality Management
permalink: /quality-management/quality-control/
---

# Quality Control

After the production/assembly stage, quality control (QC) tests are performed on every sensor to validate the data quality. QAP is a quality management procedure followed during the sensor build/assembly process, whereas QC procedures are performed after the complete build procedure and before the deployment.QC procedure helps us in testing and calibrating the device.Testing reduces the uncertanities in device performance.Calibration helps in vaidating the data

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

The purpose of this document is to provide Quality Control (QC) guidelines for the following 

1. Sensor Calibration and Data Validation Testing

2. Noise Floor Testing

## 2.0 Quality Control

### 2.1 Sensor Calibration and Data Validation Testing

#### Objective

To perform initial calibration and validate sensor data after QAP in laboratory conditions.This helps us to validate and calibrate the raw data from the sensor.

A procedure to calibrate the sensor is given below.

#### Procedure

1. Identify four different locations with different heights (h1,h2,h3,h4) from the surface using measuring tape.
2. Strating from mount location h1 place the sensor at each mount location  and collect data every 30 seconds for at least 30 minutes, totaling at least 60 measurements.This provides us enought data to understand the intrinsic noise  of the sensor and helps for calibration .
3. When sensor is at each position place an object with known height beneath the sensor for the next 30 minutes and record the measurements.This helps us to validate the measurements received by the sensor(since we know the distance of placed object the measured distance by sensor should be ground truth + or - noise).
4. Repeat the above steps for the remainng heights.

#### Calibration
The purpose of calibration is to get a single straight line in the event of no flood
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

