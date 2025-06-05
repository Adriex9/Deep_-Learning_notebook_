Dog and Cat Breed Classification with Deep Learning on The Oxford-IIIT Pet dataset
This project involves building a deep learning model for classifying dog and cat breeds using images. The model leverages the VGG16 architecture with transfer learning to achieve high accuracy on a dataset containing multiple dog and cat breeds.

Project Overview
Data Handling: The dataset consists of images of different dog and cat breeds. The initial challenge involved handling image data and working with byte strings, which was solved by using the PIL library.

Environment Setup: Initially, I worked without a powerful GPU, which led to memory issues and slow training. After upgrading to a T4 GPU on Google Colab, training performance significantly improved.



Model Architecture:
![image](https://github.com/user-attachments/assets/5acdac7a-e264-4e5d-99a0-c322fa178e48)


Started with a simple model and gradually improved it.
The model was based on VGG16 (pre-trained on ImageNet), and I fine-tuned it using data augmentation, Dropout and early stopping to avoid overfitting.
trained on 40 epochs
![image](https://github.com/user-attachments/assets/7a26e521-20e2-429b-8e9c-d81f48a42973)

then trained again on 30 more epochs witha all 10 last layers trainable 
![image](https://github.com/user-attachments/assets/ba19f012-8736-4e57-b2ae-1195fff32c6d)
head map Grad-Cam
![image](https://github.com/user-attachments/assets/a8d70f06-8f99-4aab-969b-5b027457cce4)

here the confusion matrix showing very good result and showing miss interpreation of siamese and birman for example that looks are very alike

![image](https://github.com/user-attachments/assets/e74eca06-e051-4f6e-8b27-f499ed50bd69)



Final Results: After applying the above steps, the model achieved ~84% accuracy
![image](https://github.com/user-attachments/assets/d5876e6a-9800-4628-b684-57ed5c68ec63)

Dependencies: 
-TensorFlow
-Keras
-NumPy
-Matplotlib
-scikit-learn



# 🐶🐱 Dog and Cat Breed Classification with Deep Learning  
### Using the Oxford-IIIT Pet Dataset

This project builds a deep learning model to classify dog and cat breeds using images.  
It leverages **transfer learning with VGG16** to achieve high accuracy on the **Oxford-IIIT Pet Dataset**.

---

## 📌 Project Overview

- **Dataset**: Images of 37 dog and cat breeds.
- **Goal**: Predict the correct breed based on a given image.
- **Challenge**: Efficient image preprocessing, optimizing training time, and avoiding overfitting.

---

## 🧹 Data Handling

- Used the **PIL** library to handle image data and byte strings.
- Applied **data augmentation** to improve generalization.

---

## ⚙️ Environment Setup

- Initially trained without a dedicated GPU → experienced slow performance and memory issues.
- Switched to **Google Colab with T4 GPU**, which significantly improved training time.

---

## 🧠 Model Architecture

- Started with a **simple convolutional model**, then transitioned to **VGG16 (pre-trained on ImageNet)**.
- Fine-tuned the model with:
  - `Dropout`
  - `EarlyStopping`
  - `ImageDataGenerator` for data augmentation
- Final model trained for:
  - **40 initial epochs**
  - Then **30 additional epochs** with the **last 10 layers unfrozen**

### 🧱 Architecture Diagram  
![Model Architecture](https://github.com/user-attachments/assets/5acdac7a-e264-4e5d-99a0-c322fa178e48)

---

## 📈 Training Results

### ✅ After 40 Epochs  
![Training 40 Epochs](https://github.com/user-attachments/assets/7a26e521-20e2-429b-8e9c-d81f48a42973)

### 🔁 Additional 30 Epochs (Last 10 Layers Trainable)  
![Training Fine-Tuned](https://github.com/user-attachments/assets/ba19f012-8736-4e57-b2ae-1195fff32c6d)

---

## 🔍 Model Interpretability

### 🎯 Grad-CAM Heatmap  
Used Grad-CAM to visualize model attention on input images.  
![GradCAM](https://github.com/user-attachments/assets/a8d70f06-8f99-4aab-969b-5b027457cce4)

---

## 📉 Evaluation

### Confusion Matrix  
Clearly shows high performance, with minor confusion between visually similar breeds like **Siamese** and **Birman**.  
![Confusion Matrix](https://github.com/user-attachments/assets/e74eca06-e051-4f6e-8b27-f499ed50bd69)

---

## 🏁 Final Results

- Achieved **~84% accuracy** on validation data.
- Robust against overfitting with early stopping and fine-tuning.

![Final Accuracy](https://github.com/user-attachments/assets/d5876e6a-9800-4628-b684-57ed5c68ec63)

---

## 📦 Dependencies

- `TensorFlow`
- `Keras`
- `NumPy`
- `Matplotlib`
- `scikit-learn`

> To install dependencies:
```bash
pip install tensorflow keras numpy matplotlib scikit-learn
