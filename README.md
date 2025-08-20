Perfect 👍 Here’s a **ready-to-use README.md** tailored for your project.
You can drop this into your repo as `README.md`.

---

````markdown
# 🩺 Face Mask Detection using CNN & Transfer Learning

This project implements **Face Mask Detection** using **Convolutional Neural Networks (CNNs)** and **Transfer Learning** with VGG16.  
The model classifies images into **three categories**:
- ✅ With Mask  
- ❌ Without Mask  
- ⚠️ Partial Mask  

---

## 📌 Motivation
The COVID-19 pandemic highlighted the importance of wearing face masks.  
This project demonstrates how **Deep Learning + Computer Vision** can automatically detect whether a person is wearing a mask properly.  

Applications include:
- Schools
- Hospitals
- Airports
- Public gatherings

---

## 📂 Dataset
- Dataset: [Face Mask Dataset](https://cdn.iisc.talentsprint.com/CDS/MiniProjects/MP2_FaceMask_Dataset.zip)  
- Total images: ~6,000  
- Classes:
  - `with_mask`
  - `without_mask`
  - `partial_mask`

Data is split into:
- **Training set:** 5029 images  
- **Test set:** 1059 images  

⚠️ Dataset folder (`content/`) is **ignored in Git** using `.gitignore`.

---

## ⚙️ Installation
Clone the repository:
```bash
git clone https://github.com/KruthikKoundinyas/face_mask_detection_CNN.git
cd face_mask_detection_CNN
````

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🧠 Models

### 1. Custom CNN

* 3 convolutional + pooling layers
* Dense + Dropout for classification
* Softmax output for 3 classes

### 2. Transfer Learning (VGG16)

* Pretrained on ImageNet
* Removed top layer, added custom dense layers
* Fine-tuned last 4 convolutional blocks
* Achieved **higher generalization accuracy** than custom CNN

---

## 🚀 Training

Run the notebook:

```bash
jupyter notebook Kruthik_Face_Mask_Detection_CNN.ipynb
```

Or open in **Google Colab**:

* Upload notebook
* Mount dataset (`content/`)
* Run cells sequentially

---

## 📸 Live Detection

* **In Colab** → Uses browser webcam (via `google.colab.output`).
* **In VS Code / Jupyter locally** → Updated code with **OpenCV** (`cv2`) to capture photo with **SPACE (capture)** and **ESC (exit)**.

---

## 📊 Results

* **Custom CNN:** High training accuracy (\~98%), poor validation accuracy (\~42%) → overfitting.
* **VGG16 Transfer Learning:** Better generalization, validation/test accuracy \~45–50%.
* **Partial Mask class** was most frequently misclassified (confused with With/Without mask).

---

## 📈 Future Improvements

* Use larger, more diverse dataset
* Apply stronger regularization (dropout, weight decay)
* Experiment with other pretrained models (ResNet50, MobileNetV2, EfficientNet)
* Deploy as a **web app** using Flask/Streamlit

---

## 📦 Repository Structure

```
face_mask_detection_CNN/
├─ content/                               # dataset (ignored in git)
├─ .gitignore                             # ignore rules
├─ Kruthik_Face_Mask_Detection_CNN.ipynb   # main notebook
├─ README.md                              # project description
└─ requirements.txt                       # dependencies
```

---

## 👨‍💻 Author

* **Kruthik**
  Face Mask Detection using CNN

---