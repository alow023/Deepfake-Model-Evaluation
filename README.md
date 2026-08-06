# Deepfake-Model-Evaluation
As deepfake technology rapidly evolves, there is a critical need to continuously evaluate detection solutions against real-world synthetic media. The aim of this project is to discover state-of-the-art Deepfake Detection tools to identify solutions for real-world use cases.

## 📊 Image-based Datasets

### 140k Real and Fake Faces
- **Description:** Large collection of real and AI-generated face images  
- **Size:** ~140,000 images  
- **Source:** StyleGAN-generated faces vs real faces  
- **Download:** [Kaggle Dataset]([https://www.kaggle.com/](https://www.kaggle.com/xhlulu/140k-real-and-fake-faces))  
- **Usage:** Perfect for image-based deepfake detection training

## 📌 Dataset Usage Notes
- **Ethical Use:** These datasets are for research purposes only  
- **Legal Compliance:** Ensure compliance with dataset licenses and terms of use  
- **Privacy:** Respect privacy rights of individuals in the datasets  
- **Citation:** Properly cite the original dataset papers when publishing research  

---

## 🏋️ Training

### Dataset Structure
Organize your training data in the `data` folder as follows:

data/
├── train/
│   ├── real/
│   │   ├── image1.jpg
│   │   └── image2.jpg
│   └── fake/
│       ├── fake1.jpg
│       └── fake2.jpg
└── validation/
    ├── real/
    └── fake/
