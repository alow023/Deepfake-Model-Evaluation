# Deepfake-Model-Evaluation
As deepfake technology rapidly evolves, there is a critical need to continuously evaluate detection solutions against real-world synthetic media. The aim of this project is to discover state-of-the-art Deepfake Detection tools to identify solutions for real-world use cases.

<u>Method</u>
Each detection tool will tested in the following way:
- Predict against 20k real and AI-generated face images from Kaggle, with the face being the focus of the image
- Predict against 52 real images from Kaggle and Canva, with a mix images with faces in the image and some faces not in the image. Few photos have faces being the focus of the image.
- Predict against 174 AI-generated images with various models with different generation methods with a mix images with faces in the image and some faces not in the image. Few photos have faces being the focus of the image.


### 📂 GitHub Repositories Used
3 random MIT Licensed deepfake detection GitHub Projects were selected to test against images generated from a variety of models. These repos are included as files in this repository as they contain changes not in the original repo for the purpose of testing the models.
1. [DeepfakeDetector](https://github.com/alow023/DeepfakeDetector)  
2. [AI-Generated-Video-Detector]([AI-Generated-Video-Detector/](https://github.com/alow023/AI-Generated-Video-Detector))  
3. [facetorch](https://github.com/alow023/facetorch)

The GitHub repositories referenced here build upon the original projects, incorporating supplementary evaluation code and documented prediction results.

### 📊 Kaggle dataset with images having the face as the main focus
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


## 📊 Images that mostly do not have faces as the main focus
The number of images generated for each model was subject to the limit imposed on the free generation plan
### 🤖 AI‑Generated Images from various models 
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

---
# Results
1. DeepfakeDetector

### 📊 Evaluation of images from Kaggle Dataset
[Predictions](https://github.com/alow023/DeepfakeDetector/blob/main/prediction_results.xlsx)

| Metric     | Value       |
|------------|-------------|
| Accuracy   | 0.9927      |
| Precision  | 0.9983      |
| Recall     | 0.9871      |
| F1 Score   | 0.9927      |

#### Confusion Matrix
|               | Predicted REAL | Predicted FAKE |
|---------------|----------------|----------------|
| **Actual REAL** | 9983           | 17             |
| **Actual FAKE** | 129            | 9871           |

[Confusion Matrix](https://github.com/alow023/DeepfakeDetector/blob/main/results_visualisations/confusion_matrix.png)

### 🖼️ Evaluation of self-sourced images
[Predictions](https://github.com/alow023/DeepfakeDetector/blob/main/prediction_results%20(Self%20sourced).xlsx)

| Metric     | Value       |
|------------|-------------|
| Accuracy   | 0.2301      |
| Precision  | 0           |
| Recall     | 0           |
| F1 Score   | 0           |

#### Confusion Matrix
|              | Predicted REAL | Predicted FAKE |
|--------------|----------------|----------------|
| **Actual REAL** | 52             | 0              |
| **Actual FAKE** | 174            | 0              |

[Confusion Matrix](https://github.com/alow023/DeepfakeDetector/blob/main/results_visualisations%20(Self-sourced)/confusion_matrix.png)

#### Model-specific predictions
| Generator      | Images | Correct   | Detection Rate (%) |
|----------------|--------|-----------|--------------------|
| Flux.2         | 9      | 0         | 0                  |
| GPT Image 2    | 24     | 0         | 0                  |
| Grok           | 24     | 0         | 0                  |
| Imagen         | 24     | 0         | 0                  |
| Nano Banana 2  | 31     | 0         | 0                  |
| Real           | 52     | 52        | 100                |
| Recraft V4.1   | 22     | 0         | 0                  |
| SDv3.5         | 24     | 0         | 0                  |
| Seedream 4.5   | 16     | 0         | 0                  |

---

2. AI-Generated-Video-Detector

### 📊 Evaluation of images from Kaggle Dataset
[Predictions](https://github.com/alow023/AI-Generated-Video-Detector/blob/main/prediction_results.xlsx)

| Metric     | Value       |
|------------|-------------|
| Accuracy   | 0.4856      |
| Precision  | 0.4190      |
| Recall     | 0.0748      |
| F1 Score   | 0.1269      |

#### Confusion Matrix
|               | Predicted REAL | Predicted FAKE |
|---------------|----------------|----------------|
| **Actual REAL** | 8963           | 1037           |
| **Actual FAKE** | 9252           | 748            |

[Confusion Matrix](https://github.com/alow023/AI-Generated-Video-Detector/blob/main/results_visualisations/confusion_matrix.png)

### 🖼️ Evaluation of self-sourced images
[Predictions](https://github.com/alow023/AI-Generated-Video-Detector/blob/main/prediction_results%20(Self%20sourced).xlsx)

| Metric     | Value       |
|------------|-------------|
| Accuracy   | 0.3319      |
| Precision  | 0.7949      |
| Recall     | 0.1782      |
| F1 Score   | 0.2911      |

#### Confusion Matrix
|              | Predicted REAL | Predicted FAKE |
|--------------|----------------|----------------|
| **Actual REAL** | 44             | 8              |
| **Actual FAKE** | 143            | 31             |

[Confusion Matrix](https://github.com/alow023/AI-Generated-Video-Detector/blob/main/results_visualisations%20(Self%20sourced)/confusion_matrix.png)

#### Model-specific predictions
| Generator      | Images | Correct | Detection Rate (%) |
|----------------|--------|---------|--------------------|
| Flux.2         | 9      | 0       | 0                  |
| GPT Image 2    | 24     | 6       | 25                 |
| Grok           | 24     | 6       | 25                 |
| Imagen         | 24     | 4       | 16.67              |
| Nano Banana 2  | 31     | 2       | 6.45               |
| Real           | 52     | 44      | 84.62              |
| Recraft V4.1   | 22     | 7       | 31.82              |
| SDv3.5         | 24     | 3       | 12.5               |
| Seedream 4.5   | 16     | 3       | 18.75              |

---

3. facetorch

### 📊 Evaluation of images from Kaggle Dataset
[Predictions](https://github.com/alow023/facetorch/blob/main/facetorch_results.xlsx)

| Metric     | Value       |
|------------|-------------|
| Accuracy   | 0.4941      |
| Precision  | 0.2568      |
| Recall     | 0.0019      |
| F1 Score   | 0.0038      |

#### Confusion Matrix
|               | Predicted REAL | Predicted FAKE |
|---------------|----------------|----------------|
| **Actual REAL** | 9658           | 55             |
| **Actual FAKE** | 9852           | 19             |

[Confusion Matrix](https://github.com/alow023/facetorch/blob/main/facetorch_visualisations/confusion_matrix.png)

### 🖼️ Evaluation of self-sourced images
[Predictions](https://github.com/alow023/facetorch/blob/main/facetorch_results%20(Self%20sourced).xlsx)

| Metric     | Value       |
|------------|-------------|
| Accuracy   | 0.2973      |
| Precision  | 0.7333      |
| Recall     | 0.1528      |
| F1 Score   | 0.2529      |

#### Confusion Matrix
|              | Predicted REAL | Predicted FAKE |
|--------------|----------------|----------------|
| **Actual REAL** | 66             | 16             |
| **Actual FAKE** | 244            | 44             |

[Confusion Matrix](https://github.com/alow023/facetorch/blob/main/facetorch_visualisations%20(Self%20sourced)/confusion_matrix.png)

#### Model-specific predictions
| Generator      | Images | Correct | Detection Rate (%) |
|----------------|--------|---------|--------------------|
| Flux.2         | 18     | 0       | 0                  |
| GPT Images     | 48     | 10      | 20.83              |
| Grok           | 48     | 12      | 25                 |
| Imagen         | 48     | 0       | 0                  |
| Nano Banas     | 62     | 8       | 12.9               |
| Real           | 104    | 66      | 63.46              |
| Recraft V4     | 44     | 0       | 0                  |
| SDv3.5         | 48     | 6       | 12.5               |
| Seedream       | 32     | 8       | 25                 |



