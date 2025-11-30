# <u>**Human Activity Recognition Using Multimodal Sensor Data (MHEALTH Dataset)**</u>

## <u>**Team Members**</u>
- **Aarif Zafar(aarifzafar@iisc.ac.in)**
- **Navneet Chandan (navneet1@iisc.ac.in)**
- **Siva Prasad J G (sivaprasad1@iisc.ac.in) 13-19-02-19-52-25-1-26331**
- **Anjali Sharma (anjali2@iisc.ac.in)**

---

## <u>**Problem Statement**</u>
This project aims to develop an intelligent **Human Activity Recognition (HAR)** system capable of classifying **12 daily activities** using multimodal wearable sensor data.

The system focuses on:
- Building accurate ML/DL activity classification models  
- Comparing traditional ML vs Deep Learning approaches  
- Understanding sensor contribution across body positions  
- Designing a preprocessing + modeling pipeline suitable for real-time HAR applications  

---

## <u>**Dataset Description**</u>
**Dataset:** _MHEALTH (Mobile Health) – UCI Machine Learning Repository_  
**Subjects:** 10 volunteers performing a set of controlled activities  

### **Activities (12 Classes)**
Standing, Sitting, Lying, Walking, Climbing Stairs, Waist Bends, Arm Elevation, Knee Bending, Cycling, Jogging, Running, Jumping.

### **Sensor Placement**
- **Chest:** Accelerometer + ECG  
- **Right Wrist:** Accelerometer, Gyroscope, Magnetometer  
- **Left Ankle:** Accelerometer, Gyroscope, Magnetometer  

### **Dataset Characteristics**
- **Sampling rate:** 50 Hz  
- **Format:** Multivariate time-series logs per subject  
- **Preprocessing performed:**
  - Data cleaning  
  - Null-class removal  
  - Z-score normalization  
  - Sliding window segmentation (2–5 seconds)  
  - Statistical, temporal, and frequency-based feature extraction  
  - Label encoding  

---

## <u>**High-Level Approach & Methods Used**</u>

### **1. Data Preprocessing**
- Merged logs from 10 subjects  
- Normalized all sensor channels  
- Applied sliding-window segmentation  
- Extracted features:
  - Statistical: mean, std, min/max, skewness  
  - Temporal: SMA, peak counts, zero-crossings  
  - Frequency-based: FFT energy, dominant frequencies  
  - Correlation-based features  

### **2. Models Trained**
**Traditional Machine Learning**
- **Random Forest**  
- **XGBoost**

**Deep Learning**
- **1D CNN**  
- **LSTM**  
- **Transformer**

### **3. Evaluation Metrics**
- **Accuracy**  
- **Macro F1-Score**  
- Confusion matrices for per-class insights  

---

## <u>**Summary of Results**</u>

### **Overall Model Performance**
| **Model** | **Accuracy** | **Macro F1-Score** |
|-----------|--------------|--------------------|
| **XGBoost** | ⭐ **99.42%** | ⭐ **0.9944** |
| **Random Forest** | 99.20% | 0.9922 |
| **CNN** | 99.13% | 0.9882 |
| **LSTM** | 97.45% | 0.9738 |
| **Transformer** | 90.17% | 0.8434 |

---

## <u>**Key Findings**</u>
- **XGBoost** delivered the best overall performance.  
- **Random Forest** and **CNN** showed near-perfect classification accuracy.  
- **LSTM** struggled slightly with similar activities such as *Jogging vs Running*.  
- **Transformer** underperformed due to relatively small dataset size.  
- Multimodal
