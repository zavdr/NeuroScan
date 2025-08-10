# 🧠 neuroscan — brain tumor detection (mri)

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red?logo=keras)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

a deep learning project that detects brain tumors from mri scans using **mobilenet** and a **custom cnn** — built for fast, accurate, and automated diagnosis.

---

## 🚀 highlights
- ✅ binary classification of brain mri scans  
- 🧠 mobilenet (transfer learning) + custom cnn  
- 📊 70/15/15 train • val • test split  
- ⏳ early stopping + model checkpointing  
- 📈 accuracy/loss visualizations on unseen data  

---

## 📁 dataset
- **classes:** brain tumor | healthy  
- manually split + preprocessed into:
  - train  
  - val  
  - test  

---

## 🛠 model architectures
**1️⃣ custom cnn**  
- stacked conv2d + maxpooling layers  
- dense layer with sigmoid activation for binary output  

**2️⃣ mobilenet (transfer learning)**  
- pretrained on imagenet (frozen base)  
- custom classifier: flatten → dense(1, sigmoid)  

---

## ⚙️ training details
- **optimizer:** adam / rmsprop  
- **loss:** binary_crossentropy  
- **epochs:** 30  
- **callbacks:** earlystopping (val_accuracy), modelcheckpoint (best model only)  
