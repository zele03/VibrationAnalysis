# Vibration Acquisition and Analysis System

A LabVIEW-based system for real-time vibration acquisition, signal processing and offline analysis using National Instruments data acquisition hardware and a piezoelectric accelerometer.

## Project Overview

This project was developed as part of the course **Real-Time Control Algorithms** at the Faculty of Technical Sciences, University of Novi Sad.

The system enables vibration measurement, real-time signal visualization and analysis in both the time and frequency domains. It consists of two separate LabVIEW Virtual Instruments (VIs): one for real-time data acquisition and recording, and another for offline analysis of previously recorded measurements.

## System Architecture

The measurement chain consists of:

- **PCB 352C33** – piezoelectric ICP accelerometer
- **NI 9234** – dynamic signal acquisition module with IEPE excitation
- **NI WLS-9163** – wireless sensor network carrier
- **NI-DAQmx** – hardware communication and acquisition driver
- **LabVIEW** – graphical programming and signal processing environment

## Main Features

### 1. Real-Time Vibration Acquisition

- Continuous vibration data acquisition using NI-DAQmx and DAQ Assistant.
- Real-time signal visualization in the time domain.
- RMS (Root Mean Square) calculation.
- Peak-to-Peak measurement.
- Frequency spectrum analysis using FFT.
- Hanning windowing to reduce spectral leakage.
- Dominant frequency detection.
- Configurable RMS threshold and vibration status indication.
- Measurement recording in LVM format.

### 2. Offline Vibration Analysis

- Loading previously recorded LVM measurement files.
- Time-domain signal visualization.
- RMS and Peak-to-Peak calculations.
- FFT-based frequency analysis.
- Dominant frequency identification.
- Re-analysis of recorded measurements without requiring connected acquisition hardware.

## Signal Processing

The system extracts several key parameters from the measured vibration signal:

| Parameter | Description |
|---|---|
| RMS | Effective vibration acceleration |
| Peak-to-Peak | Difference between maximum and minimum acceleration |
| FFT Spectrum | Frequency-domain representation of the signal |
| Dominant Frequency | Frequency corresponding to the maximum spectral magnitude |
| RMS Threshold | Configurable threshold for vibration level indication |

## Acquisition Configuration

| Parameter | Value |
|---|---|
| Measurement type | Acceleration |
| Acquisition channel | ai0 |
| Sampling rate | 25,600 Hz |
| Samples per block | 25,600 |
| Sensor sensitivity | 100 mV/g |
| IEPE excitation | 2 mA |
| Signal coupling | AC |
| FFT measurement | Magnitude (Peak) |
| Window function | Hanning |

## Technologies and Tools

- LabVIEW
- NI-DAQmx
- NI MAX (Measurement & Automation Explorer)
- FFT and digital signal processing
- National Instruments data acquisition hardware

## Authors

**Luka Zelembaba**  
**Dušan Đurić**

Faculty of Technical Sciences, University of Novi Sad  
Course: Real-Time Control Algorithms

## Documentation

Detailed technical documentation covering hardware configuration, acquisition setup, signal processing methods and software implementation is available in the `docs/` directory.
