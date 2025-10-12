# 🧠 Brain Tumor MRI Classification with Explainable AI (XAI)

Brain tumor classification plays a critical role in early diagnosis and treatment planning. MRI imaging is a primary tool for detecting different types of brain tumors, but manual analysis can be time-consuming and prone to errors.  
This project introduces a **hybrid ensemble framework** that combines **deep learning (CNN)** and **traditional machine learning (ML)** models to enhance classification accuracy and interpretability through Explainable AI (XAI) techniques.

> ⚡ *Key Models:* ResNet50V2, DenseNet121, EfficientNetB0  
> 🧭 *Key XAI Techniques:* Grad-CAM, SHAP, Ensemble Consensus Analysis

---

## 🚀 Project Overview

- Developed a **hybrid ensemble model** combining CNN and classical ML approaches.
- Achieved **89.3% overall accuracy**, with top individual model accuracy of **97% (DenseNet121)**.
- Incorporated **Grad-CAM** for visual interpretability and **SHAP** for feature attribution.
- Conducted **ensemble consensus analysis** to evaluate prediction reliability for clinical use.
- Provided comprehensive performance analysis, highlighting strengths and limitations of different tumor classifications.

---

## 📊 Explainable AI Components

### 🟥 1. Grad-CAM: Visual Region Analysis
- Highlights discriminative brain regions that influence CNN decisions.
- Applied to the final convolutional layers of **ResNet50V2**, **EfficientNetB0**, and **DenseNet121**.
- Reveals distinct activation patterns across tumor types:
  - Posterior activations for focused cases.
  - Multi-regional activations for complex tumors.
  - Central activations for deep-seated tumors.

---

### 🟦 2. SHAP: Feature Attribution
- Analyzes **global and local feature contributions** using Shapley values.
- Key discriminative features:
  - **Gray Level Std. Dev.** — highest discriminative power across SHAP and LIME.
  - **Sobel Edge Intensity** & **Hu Moments** — emphasized by Gradient Boosting for structure.
- CNN features provide complementary spatial cues, validating the hybrid design.

---

### 🟩 3. Ensemble Consensus Analysis
- Assesses prediction reliability through **agreement levels** across models:

| Consensus Level        | Distribution | Accuracy | Clinical Protocol                          |
|-------------------------|-------------:|---------:|--------------------------------------------|
| 🟢 Perfect Consensus     | 50.0%        | 85.0%    | Automated decision-making                  |
| 🟡 Majority Consensus    | 30.0%        | 85.0%    | Additional validation                      |
| 🔴 No Consensus          | 20.0%        | 65.0%    | Mandatory expert review                    |

- Perfect alignment enables automated diagnosis, while low consensus highlights challenging cases.

---

## 🧪 Performance Highlights

| Model              | Accuracy | Notable Performance                        |
|---------------------|---------:|---------------------------------------------|
| DenseNet121         | 97%      | Best individual CNN                        |
| ResNet50V2          | 96%      | Strong feature localization                 |
| Hybrid Ensemble     | 89.3%    | Balanced performance across tumor classes  |

- **Best Class:** Pituitary Tumor (F1-score 0.94)  
- **Challenging Class:** Meningioma (Recall 0.81)  
- **Misclassifications:** Primarily between glioma and meningioma due to overlapping features.

---

## 🛠️ Tech Stack

- **Programming Language:** Python  
- **Deep Learning:** TensorFlow / Keras  
- **Machine Learning:** Scikit-learn, XGBoost  
- **XAI:** Grad-CAM, SHAP  
- **Visualization:** Matplotlib, Seaborn  
- **Data Handling:** NumPy, Pandas

---

## 🧑‍🏫 Acknowledgment

This project was conducted as part of my research on **explainable medical AI**, aiming to support **clinicians in diagnostic decision-making**. The hybrid ensemble framework and XAI analysis contribute toward developing transparent and reliable AI systems for healthcare.

---
