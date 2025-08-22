````markdown
# 🩺 Face Mask Detection using CNN & Transfer Learning

This project implements **Face Mask Detection** using **Convolutional Neural Networks (CNNs)** and **Transfer Learning** (VGG16).  
The model classifies images into **three categories**:
- ✅ With Mask  
- ❌ Without Mask  
- ⚠️ Partial Mask  

---

## 📌 Motivation
The COVID-19 pandemic highlighted the importance of wearing face masks.  
This project demonstrates how **Deep Learning + Computer Vision** can automatically detect whether a person is wearing a mask correctly.  

Applications:
- Schools & Universities  
- Hospitals & Healthcare  
- Airports & Railway Stations  
- Public gatherings & Offices  

---

## 📂 Dataset
- Dataset: [Face Mask Dataset (IISc TalentSprint)](https://cdn.iisc.talentsprint.com/CDS/MiniProjects/MP2_FaceMask_Dataset.zip)  
- Total images: ~6,000  
- Classes:
  - `with_mask`
  - `without_mask`
  - `partial_mask`

Data split:
- **Training:** 5029 images  
- **Testing:** 1059 images  

⚠️ Note: live test folder (`content/`) and data set folder (`MP2_FaceMask_Dataset/`) is **excluded from Git** via `.gitignore`.

---

## ⚙️ Installation
Clone the repository:
```bash
git clone https://github.com/KruthikKoundinyas/face_mask_detection_CNN.git
cd face_mask_detection_CNN
````

Create and activate a virtual environment (recommended):

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🧠 Models

### 1. Custom CNN

* 3 Convolution + MaxPooling layers
* Flatten + Dense + Dropout layers
* Softmax activation for 3 classes

### 2. Transfer Learning (VGG16)

* Pretrained on **ImageNet**
* Removed top classifier, added custom dense layers
* Fine-tuned last convolutional blocks
* Achieved **higher generalization accuracy** compared to custom CNN

---

## 🚀 Training & Usage

### Run locally (Jupyter Notebook):

```bash
jupyter notebook Kruthik_Face_Mask_Detection_CNN.ipynb
```

### Run on Google Colab:

1. Upload the notebook
2. Mount dataset inside `/content/`
3. Run cells sequentially

---

## 📸 Live Detection

* **Google Colab** → Uses browser webcam (`google.colab.output`).
* **Local (VS Code / Jupyter)** → OpenCV (`cv2`) captures webcam input:

  * Press **SPACE** → capture frame
  * Press **ESC** → exit

---

## 📊 Results

* **Custom CNN:**

  * Training accuracy \~98%
  * Validation accuracy \~42% → strong overfitting

* **VGG16 Transfer Learning:**

  * Validation/Test accuracy \~45–50%
  * Better generalization compared to CNN

* **Most common error:**

  * Misclassification of **Partial Mask** (confused with With/Without Mask).

---

## 📈 Future Work

* Train on a larger & more diverse dataset
* Stronger regularization (Dropout, L2 weight decay, Data Augmentation)
* Try other pretrained models (ResNet50, MobileNetV2, EfficientNet)
* Real-time deployment as a **Web App** (Flask / Streamlit) or **Mobile App** (TensorFlow Lite)

---

## 📦 Repository Structure

```
face_mask_detection_CNN/
├── content/                               # dataset (ignored in Git)
├── .gitignore                             # ignore rules
├── Kruthik_Face_Mask_Detection_CNN.ipynb  # main notebook
├── README.md                              # project description
└── requirements.txt                       # dependencies
```

---

## 👨‍💻 Author

**Kruthik Koundinya**
Face Mask Detection using CNN & Transfer Learning

```