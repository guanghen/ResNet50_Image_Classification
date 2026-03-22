# 🚀 ResNet50 Image Classification (COCO Dataset)

A custom image classifier built with PyTorch and the ResNet50 architecture. This project leverages transfer learning on the COCO 2017 dataset to accurately identify five specific target classes: bicycles, cats, bananas, beds, and traffic lights.

The core design philosophy of this project is to separate heavy data processing and model training from lightweight, rapid inference. Whether you are a developer looking to explore the training pipeline or a user wanting to test the model's accuracy out-of-the-box, this repository provides a seamless experience.

---

## 🌟 Key Features

*   **Automated Data Pipeline:** The training notebook integrates `pycocotools` to automatically parse annotations and fetch only the necessary images for the target classes, eliminating the need to download the massive, full COCO dataset locally.
*   **Transfer Learning:** Utilizes a pre-trained ResNet50 model to extract features, modifying the fully connected layer for a 5-class fine-tuning process. This significantly reduces training time and improves convergence.
*   **Zero-Configuration Inference:** Features a standalone Quick Test script that automatically pulls pre-trained weights and runs predictions. No local GPUs or complex environment setups are required to test the model.

---

## 🚀 Quick Start

This project is optimized for Google Colab. Click the badges below to run the code directly in your browser.

### Option A: Run Inference (Recommended for Quick Testing)
Launch the inference notebook to immediately test the model. It automatically downloads the pre-trained weights and randomly samples images from the `test_examples` folder to display multi-label predictions with confidence scores.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guanghen/ResNet50_Image_Classification/blob/main/Quick_Test.ipynb)

### Option B: Train from Scratch
Launch the training notebook to explore the entire lifecycle, including dataset downloading, preprocessing, and model fine-tuning.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guanghen/ResNet50_Image_Classification/blob/main/Train_ResNet50_COCO.ipynb)

---

## 📁 Repository Structure

```text
├── Train_ResNet50_COCO.ipynb    # Core training pipeline (Data fetching, preprocessing, fine-tuning)
├── Quick_Test.ipynb             # Lightweight inference (Weight loading, random sampling, visualization)
├── dataset_manifest_cleaned.csv # Cleaned metadata for the target dataset
├── requirements.txt             # Project dependencies
└── test_examples/               # Directory containing 100 sample images across the 5 classes
(Note: The pre-trained model weights resnet50_coco_model.pth are hosted in the Releases section of this repository.)
```
## 🛠️ Tech Stack

* **Deep Learning:** PyTorch, Torchvision
* **Data Processing:** Pandas, NumPy, pycocotools
* **Visualization:** Matplotlib, PIL
* **Architecture:** ResNet50 (Pre-trained on ImageNet)

---

## 💻 Local Setup

If you prefer to run this project in your local environment:

1. Clone the repository:
   ```bash
   git clone [https://github.com/guanghen/ResNet50_Image_Classification.git](https://github.com/guanghen/ResNet50_Image_Classification.git)
   cd ResNet50_Image_Classification
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Launch Jupyter Notebook and open either .ipynb file to get started.
