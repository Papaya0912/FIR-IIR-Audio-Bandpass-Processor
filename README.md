# 🎛️ Digital Audio Signal Processing: FIR & IIR Filter Design

![Language](https://img.shields.io/badge/Language-Python-blue.svg)
![Domain](https://img.shields.io/badge/Domain-Digital%20Signal%20Processing-orange.svg)
![Library](https://img.shields.io/badge/Library-SciPy-success.svg)

## 📌 Overview
This project is a comprehensive Digital Signal Processing (DSP) tool designed to extract audio from video files and apply custom mathematical bandpass filters (500Hz - 2000Hz). It implements and compares two fundamental filtering techniques: **FIR (Finite Impulse Response) using a Kaiser window** and **IIR (Infinite Impulse Response) using an analog Butterworth filter with Bilinear Transformation**.

## 🚀 Key Features
* **Automated Audio Extraction:** Seamlessly extracts `.wav` stereo audio from `.mp4` video inputs using `moviepy`.
* **Custom Filter Design from Scratch:** * Mathematically calculates filter parameters (Order `N`, `beta`) for the FIR Kaiser window based on strict passband and stopband attenuation requirements.
  * Designs analog IIR Butterworth filters and converts them to digital using the Bilinear Transform.
* **Cascade Filtering (Bandpass):** Achieves the target frequency range (500Hz - 2000Hz) by cascading meticulously designed Lowpass and Highpass filters on both Left and Right audio channels.
* **Rich Visualizations:** Plots exact Magnitude Responses (Bode plots) for the designed filters and compares the Fast Fourier Transform (FFT) spectrums of the Original, FIR-filtered, and IIR-filtered audio signals.

## 🛠️ Tech Stack & Libraries
* **SciPy (`scipy.signal`, `scipy.io`):** Core library for DSP operations, signal filtering (`lfilter`), and filter design (`firwin`, `butter`, `bilinear`).
* **NumPy:** High-performance matrix and mathematical operations for audio data arrays.
* **Matplotlib:** Frequency domain (FFT) and magnitude response visualizations.
* **MoviePy:** Video and audio I/O operations.
