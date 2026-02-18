# 📦 Robocon Box Real/Fake Detection

![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

<p align="center">
  <strong>A Deep Learning solution for the Robocon competition to classify boxes as "Real" or "Fake".</strong>
</p>

---

## 📖 Table of Contents
- [About the Project](#-about-the-project)
- [Key Features](#-key-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [Model Architecture](#-model-architecture)
- [Results & Verification](#-results--verification)
- [Optimization Tips](#-optimization-tips)

---

## 🔍 About the Project

This repository hosts a robust **Convolutional Neural Network (CNN)** built with **TensorFlow** and **Keras** designed to distinguish between "Real" and "Fake" boxes. Originally developed for the **Robocon competition**, this model ensures high accuracy in object classification tasks essential for autonomous robotics.

The project includes a complete training pipeline within a Jupyter Notebook, covering data preprocessing, model training, evaluation, and real-time prediction verification.

---

## ✨ Key Features

- **Binary Classification**: Accurately classifies images into two categories: `Real` vs `Fake`.
- **Data Augmentation**: (Implicit in `image_dataset_from_directory` pipeline) Efficient data loading and caching for performance.
- **Visual Verification**: Includes a built-in verification tool to inspect model predictions against actual labels.
- **Portable**: Configured to run locally with relative paths, removing dependency on specific cloud environments (like Kaggle).

---

## 📂 Project Structure

```bash
Robocon_Box_detection_real_fake/
├── README.md              # Project documentation
├── realfake.ipynb         # Main Jupyter Notebook for training & inference
├── requirements.txt       # Python dependencies
├── .gitignore             # Git ignore rules
└── dataset/               # Image dataset directory
    ├── real/              # Training images for 'Real' boxes
    └── fake/              # Training images for 'Fake' boxes
```

---

## 🚀 Getting Started

Follow these steps to set up the project locally.

### Prerequisites

Ensure you have **Python 3.11+** installed. You will also need:
- TensorFlow
- NumPy
- Matplotlib
- Jupyter

### Installation

1.  **Clone the repository**
    ```bash
    git clone <repository_url>
    cd Robocon_Box_detection_real_fake
    ```

2.  **Create a virtual environment (Optional but recommended)**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3.  **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

---

## 💻 Usage

1.  **Prepare your dataset**:
    Ensure your images are organized in the `dataset/` folder as follows:
    - Put "Real" box images in `dataset/real/`
    - Put "Fake" box images in `dataset/fake/`

2.  **Launch the Notebook**:
    ```bash
    jupyter notebook realfake.ipynb
    ```

3.  **Train & Predict**:
    - Run all cells in the notebook.
    - The model will train for the specified epochs.
    - At the end, a **Verification Cell** will display random images with their actual and predicted labels for visual confirmation.

---

## 🧠 Model Architecture

The custom CNN architecture is optimized for speed and accuracy:

1.  **Input Layer**: Rescaling (Normalizes pixel values to [0, 1]).
2.  **Feature Extraction**:
    - 3x Convolutional Blocks (`Conv2D` + `MaxPooling2D`).
    - Uses `ReLU` activation for non-linearity.
3.  **Classification Head**:
    - `Flatten` layer.
    - `Dense` layer (128 units, ReLU).
    - `Dropout` (0.5) to prevent overfitting.
    - `Dense` Output layer (Sigmoid activation) for binary probability.

---

## 📊 Results & Verification

The model provides a confidence score for each prediction:

- **Result: REAL** (e.g., Confidence: 0.95)
- **Result: FAKE** (e.g., Confidence: 0.88)

You can instantly verify model performance using the integrated visualization tool in the notebook:

![Verification Example](https://via.placeholder.com/800x200?text=Verification+Cell+Output+Placeholder)  
*(The notebook will generate a real grid of images like this)*

---

## 💡 Optimization Tips

> [!TIP]
> **Capture Your Own Data**: For the best performance in the actual competition arena, avoid relying solely on downloaded datasets. **Train the model using images captured from the actual camera** you will use on the robot. This ensures the neural network adapts to your specific:
> - Camera lens distorion
> - Perspective and mounting height
> - Arena lighting conditions

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.
