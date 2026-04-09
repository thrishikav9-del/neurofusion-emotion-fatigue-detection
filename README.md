# NeuroFusion: Multimodal Emotion & Fatigue Detection System

## Overview

NeuroFusion is an AI-driven multimodal system designed to detect human emotional states and mental fatigue in real time using physiological signals. The system integrates multiple biosignal modalities to provide a comprehensive and accurate assessment of cognitive and emotional conditions.

Unlike traditional single-modality approaches, NeuroFusion combines EEG, fNIRS, ECG, and EMG signals into a unified framework, enabling robust detection and real-time intervention capabilities. 

---

## Key Contributions

* Multimodal fusion of EEG, fNIRS, ECG, and EMG signals
* Real-time emotion and fatigue detection (<250 ms latency)
* Hybrid machine learning architecture (CNN + LSTM + classical ML)
* Feature engineering across 383 physiological features
* Achieved **87.5% classification accuracy**
* Adaptive feedback system for user intervention

---

## Problem Statement

Modern digital environments lead to increased mental fatigue and emotional stress due to prolonged screen exposure and cognitive overload.

Existing systems:

* Use single biosignal modality
* Lack real-time processing
* Fail to integrate emotion and fatigue jointly

NeuroFusion addresses these limitations by providing a **real-time, multimodal, AI-based detection system**.

---

## System Architecture

The system follows a **4-stage processing pipeline**:

### 1. Data Acquisition

* Simultaneous recording of:

  * EEG (8 channels)
  * fNIRS (48 channels)
  * ECG
  * EMG
* Synchronized multi-sensor data collection

### 2. Signal Processing

* Noise filtering and artifact removal
* Feature extraction (time, frequency, statistical features)
* Signal quality validation

### 3. Intelligent Analysis

* Feature selection (top discriminative features)
* Hybrid ML model:

  * CNN for feature extraction
  * LSTM for temporal modeling
  * SVM / Random Forest for classification

### 4. Adaptive Feedback

* Fatigue prediction (0–1 scale)
* Real-time recommendations:

  * Break suggestions
  * Breathing exercises
  * Workload adjustments

---

## Technology Stack

* Python
* NumPy, SciPy (Signal Processing)
* Scikit-learn (ML models)
* Deep Learning (CNN + LSTM)
* Matplotlib (Visualization)

---

## Dataset

* Source: IEEE Dataport – MULTIDATA
* Multimodal biosignal dataset
* 16 participants (ages 22–34)
* 64 sessions (~48 hours of data)
* Includes EEG, fNIRS, ECG, and EMG signals
* Labeled with emotion and fatigue levels 

---

## Methodology

### Signal Acquisition

* EEG: 8-channel (512 Hz)
* fNIRS: 48-channel (16 Hz)
* ECG: Lead II configuration
* EMG: Facial muscle activity

### Feature Engineering

* EEG band powers (alpha, beta, etc.)
* HRV features from ECG
* Hemoglobin concentration (fNIRS)
* EMG RMS and signal envelope

### Machine Learning Pipeline

* Feature normalization (Z-score)
* Dimensionality reduction (PCA)
* Feature selection (ANOVA + RFE)
* Classification:

  * SVM
  * Random Forest
* Temporal modeling:

  * Hidden Markov Models / LSTM

---

## Results

According to the evaluation results:

* Accuracy: **87.5%**
* Real-time latency: **<250 ms**
* Reliable classification across participants

👉 As shown in the confusion matrix (page 21), the model achieves high correct predictions for both fatigue and non-fatigue states. 

👉 Feature importance analysis (page 22) highlights EEG and fNIRS features as dominant contributors. 

---

## Example Output

**Input:** Multimodal physiological signals

**Output:**

* Fatigue Probability: 0.992
* Prediction: Fatigue
* Confidence: High

**Recommendation:**

* Take a 15-minute break
* Perform breathing exercises
* Hydrate and adjust posture

👉 Sample output reports are shown in pages 24–25 of the report. 

---

## Applications

* Workplace productivity monitoring
* Driver drowsiness detection
* Healthcare and mental wellness systems
* Human-computer interaction (adaptive systems)
* Smart wearable devices

---

## Advantages

* Multimodal approach improves accuracy
* Real-time detection and intervention
* Scalable and extensible architecture
* Combines physiological and behavioral insights

---

## Limitations

* Requires specialized hardware (EEG, fNIRS)
* Complex data acquisition setup
* Computational overhead for real-time processing

---

## Future Work

* Real-time wearable integration
* Deployment on edge devices
* Deep learning-based multimodal fusion
* Personalized fatigue prediction models
* Integration with mobile applications

---

## 📄 Documentation

* Project Report: (add PDF here)

---

## Disclaimer

This project is developed for academic and research purposes. It is intended to support human well-being and should not be misused.

---

## Authors

Thrishika and Team
B.Tech CSE (AI)
