# Deepfake-Model-Evaluation
As deepfake technology rapidly evolves, there is a critical need to continuously evaluate detection solutions against real-world synthetic media. The aim of this project is to discover state-of-the-art Deepfake Detection tools to identify solutions for real-world use cases.

### 📂 GitHub Repositories Used
3 random MIT Licensed deepfake detection GitHub Projects were selected to test against images generated from a variety of models
- [DeepfakeDetector](https://github.com/TRahulsingh/DeepfakeDetector)  
- [AI-Generated-Video-Detector](https://github.com/Pranesh-2005/AI-Generated-Video-Detector)  
- [facetorch](https://github.com/tomas-gajarsky/facetorch/blob/main/README.md)


### 📊 Image-based Datasets
This dataset was used to train models from the GitHub repositories
#### 140k Real and Fake Faces
- **Description:** Large collection of real and AI-generated face images  
- **Size:** ~140,000 images  
- **Source:** StyleGAN-generated faces vs real faces  
- **Download:** [Kaggle Dataset]([https://www.kaggle.com/](https://www.kaggle.com/xhlulu/140k-real-and-fake-faces))  
- **Usage:** Perfect for image-based deepfake detection training

### 📌 Dataset Usage Notes
- **Ethical Use:** These datasets are for research purposes only  
- **Legal Compliance:** Ensure compliance with dataset licenses and terms of use  
- **Privacy:** Respect privacy rights of individuals in the datasets  
- **Citation:** Properly cite the original dataset papers when publishing research  


## 📊 Images for testing detection tools
The number of images generated for each model was subject to the limit imposed on the free generation plan
### 🤖 AI‑Generated Models
| Model          | Number of Images | Generation Method                  |
|----------------|------------------|------------------------------------|
| Recraft v4.1   | 22               | Diffusion + vector hybrid          |
| Seedream 4.5   | 16               | Diffusion with semantic guidance   |
| SDv3.5         | 24               | Diffusion (Stable Diffusion)       |
| Nano Banana 2  | 31               | Web‑grounded multimodal diffusion  |
| GPT‑Image‑2    | 24               | Diffusion (successor to DALL·E)    |
| Flux.2         | 9                | Diffusion + transformer hybrid     |
| Imagen         | 24               | Autoregressive + diffusion hybrid  |
| Grok           | 24               | Transformer‑based multimodal model |

**Subtotal (AI‑Generated): 174 images**

### 🏞️ Real Images
| Source         | Number of Images | Notes                  |
|----------------|------------------|------------------------|
| Kaggle         | 38               | Real face dataset      |
| Canva          | 14               | Stock photography      |

**Subtotal (Real): 52 images**

#### Total
**226 images (174 AI‑generated + 52 real)**



---

### 🏋️ Training

#### Dataset Structure
Organize your training data in the `data` folder as follows:
```
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
```
