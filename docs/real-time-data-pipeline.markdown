---
layout: default
title: Real-time Data Pipeline
permalink: /real-time-data-pipeline/
---

# Real-time Data Pipeline

- [1.0 General](#10-general)
  * [1.1 Background](#11-background)
  * [1.2 Purpose](#12-purpose)
- [2.0 Considerations/Limitations](#20-considerations-limitations)
- [2.1 Ground truth Validation of Real-time Flood Depth Data](#21-ground-truth-validation-of-real-time-flood-depth-data)
  * [2.2 Sensor Deployment Considerations](#22-sensor-deployment-considerations)
    + [2.2.1 Error in Pole Mount Angles](#221-error-in-pole-mount-angles)
    + [2.2.2 Location and Surface](#222-location-and-surface)
    + [2.2.3 Obstacles](#223-obstacles)
  * [2.3 Hardware Limitations](#23-hardware-limitations)
    + [2.3.1 Accuracy of Ultrasonic Sensor](#231-accuracy-of-ultrasonic-sensor)
    + [2.3.2 Noise Floor of Ultrasonic Sensor](#232-noise-floor-of-ultrasonic-sensor)
    + [2.3.3 Seasonal and Temperature Drift](#233-seasonal-and-temperature-drift)
    + [2.3.4 Influence on Ultrasonic Raw measurements by external factors](#234-influence-on-ultrasonic-raw-measurements-by-external-factors)
- [3.0 Flood Depth Data Flow Pipeline](#30-flood-depth-data-flow-pipeline)
  * [3.1 Data Flow Pipeline Overview](#31-data-flow-pipeline-overview)
  * [3.2 Data Processing Methodology](#32-data-processing-methodology)
    + [Message Syntax Check - TTN Console](#message-syntax-check---ttn-console)
    + [Distance to Depth Conversion](#distance-to-depth-conversion)
    + [Erroneous Depth Data Filter](#erroneous-depth-data-filter)
    + [Data Storage - InfluxDB](#data-storage---influxdb)
    + [Offset Calculator](#offset-calculator)
- [References](#references)

## 1.0 General

### 1.1 Background

This project uses advanced IoT flood sensors to measure Real-time Flood Depth Data (FDD) on a city-wide scale using [Industrial grade Ultrasonic](https://www.maxbotix.com/ultrasonic_sensors/mb7389.htm) ranging technology. The Ultrasonic rangefinder readings are distance measurements and they are passed through a real-time data pipeline to calculate depth measurements.

### 1.2 Purpose

The purpose of this document is to explain the Real-time Flood Depth Data pipeline and methodology. 

## 2.0 Considerations/Limitations

This section details the important considerations and limitations of the Flood Depth Data quality. 

## 2.1 Ground truth Validation of Real-time Flood Depth Data

To manually validate the Real-time Flood Depth Data, the FloodNet researchers have conducted a Manual Validation Experiment during the event of a flood on the July 23 at 8:30pm in {location}. Manual depth calculation is performed by manually capturing the depth readings from a standard measuring scale that has been installed on the same pole on which the sensor has been mounted.

<img src="/assets/images/floodnet-researchers-in-action.jpg" width="400"/>

The following figure shows the comparision of manual depth captured vs Flood-Depth Data processed from the Data-pipeline. The results verify the validation of the Flood Depth Data captured by the Real-time Flood Monitoring System.

<figure>
  <img
  src="/assets/images/manual-validation-plot.png"
  alt="validation plot">
</figure>



### 2.2 Sensor Deployment Considerations

#### 2.2.1 Error in Pole Mount Angles 

Error in Light pole angles, street sign post angles

#### 2.2.2 Location and Surface

#### 2.2.3 Obstacles

Weeds, dogs, humans, animals

### 2.3 Hardware Limitations

#### 2.3.1 Accuracy of Ultrasonic Sensor

#### 2.3.2 Noise Floor of Ultrasonic Sensor

#### 2.3.3 Seasonal and Temperature Drift 

#### 2.3.4 Influence on Ultrasonic Raw measurements by external factors

## 3.0 Flood Depth Data Flow Pipeline

### 3.1 Data Flow Pipeline Overview

The following figure shows the overview of the Data Flow Pipeline: 

![datapipeline-overview](/assets/images/data-pipeline-overview.png)

The Flood Sensors transmit the raw data packets over LoRaWAN. These packets are forwarded to a The Things Network (TTN) application via LoRa Gateway. This data is further flows from the TTN into open-source tools hosted on NYU servers for further processing and storage. A combination of docker containers is running a load-balanced web server (NGINX), certificate authority (LetsEncrypt), data routing layer (NodeRed), a database (InfluxDB), and a dashboard platform (Grafana).

The data processing stage takes place on the Node-RED flow, where the raw distance measurements are converted into Flood Depth Data (FDD).

Raw as well as processed data is stored in the InfluxDB database. From there, Grafana handles all the visualization and alerting through its intuitive dashboarding platform. 

### 3.2 Data Processing Methodology

![full-data-pipeline](/assets/images/full-data-pipeline.png)

#### Message Syntax Check - TTN Console

Payload decoder has been implemented on the TTN console to check and verify the payload of the incoming messages from the end-nodes.

#### Distance to Depth Conversion

The raw measurements of the ultrasonic sensors are distances. Depth measurements are calculated via two transformations - Inversion followed by Offsetting. Inversion is multiplying the distance measurements with negative one. Offsetting is adding an offset value to the inverted measurements to obtain depth measurements.

#### Erroneous Depth Data Filter

#### Data Storage - InfluxDB

#### Offset Calculator

## References

1. [U.S. Integrated Ocean Observing System, 2021. Manual for Real-Time Quality Control of Water Level Data Version 2.1](https://doi.org/10.25923/vpsx-dc82)
2. [NWS Techniques Specification Package (TSP) 88-21-R2 (1994)](ftp://ftp.library.noaa.gov/noaa_documents.lib/NWS/NWS_TSP_88-21-R2.pdf)
3. [Maxbotix HRXl-MaxSonar -WR Datasheet](https://www.maxbotix.com/documents/HRXL-MaxSonar-WR_Datasheet.pdf)
4. [New York City Department of Transportation Traffic Signal Standard Drawings](https://www1.nyc.gov/html/dot/downloads/pdf/nyc-dot-traffic-signal-standard-drawings.pdf)
5. [New York State Standard Sheets](https://www.dot.ny.gov/main/business-center/engineering/specifications/busi-e-standards-usc/usc-repository/2017_9_stdsht_usc_book%204.pdf)
6. [LoRaWAN Class A Devices](https://lora-developers.semtech.com/uploads/documents/files/LoRaWAN_Class_A_Devices_In_Depth_Downloadable.pdf)
