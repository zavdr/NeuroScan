# 🧠 NeuroScan: Brain Tumor Detection from MRI Using Deep Learning

NeuroScan is a deep learning project that detects brain tumors from MRI scans using a Convolutional Neural Network (CNN). It classifies MRI images into two categories  **(Brain Tumor** and **Healthy)**, providing a powerful tool for early and automated medical diagnosis.

---

## 🚀 Project Highlights

- ✅ Binary image classification of brain MRI scans
- 🧠 Uses **MobileNet** with transfer learning and a custom CNN model
- 🗂 Dataset split into 70% training, 15% validation, and 15% testing
- 📉 Includes early stopping and model checkpointing
- 📊 Accuracy/Loss visualizations and evaluation on unseen data

---

## 📁 Dataset

The dataset consists of MRI scan images in two categories:

- `Brain Tumor`
- `Healthy`

> The dataset is manually split and preprocessed into `train`, `val`, and `test` folders.

---

## 🔧 Model Architectures

### 1. Custom CNN:
- Multiple `Conv2D` + `MaxPooling` layers
- Final `Dense` layer with sigmoid activation for binary classification

### 2. Transfer Learning with MobileNet:
- Base: MobileNet (pre-trained on ImageNet)
- Custom classifier head: `Flatten → Dense(1, sigmoid)`

> Only the classifier head is trainable; the MobileNet base is frozen.

---

## 📈 Training Details

- Optimizer: `Adam` / `RMSProp`
- Loss: `binary_crossentropy`
- Epochs: 30
- Callbacks:
  - `ModelCheckpoint` to save the best model
  - `EarlyStopping` based on validation accuracy
