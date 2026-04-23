# Garlic vs Grape Image Classification System

Custom CNN + Transfer Learning + Hierarchical Modeling + Adaptive Confidence Thresholding + TensorFlow Lite Preparation

---

## 1. Overview

This project explores a deep learning workflow for classifying garlic- and grape-related images using both fine-grained category labels and higher-level grouping. The repository includes structured dataset splits, model development in Jupyter Notebook, comparative experimentation with convolutional neural network approaches, and preparation for lightweight deployment.

Rather than treating the task as a simple toy classifier, the project is structured to study:

- dataset preparation and organisation
- transfer learning baselines
- custom CNN development
- model comparison and tuning
- hierarchical class reasoning
- confidence-based handling of uncertain or out-of-scope predictions
- TensorFlow Lite conversion for lightweight inference

---

## 2. Dataset Structure

The dataset is organised into training, validation, and test splits.

### Fine-grained categories
- `garlic_bulb`
- `garlic_clove`
- `grape_green`
- `grape_other`

This structure supports both:
- **fine-grained classification** across the four visible categories, and
- **coarse-grained classification** at the higher level of garlic vs grape.

The dataset pipeline is intended to improve robustness under realistic image variation such as changes in lighting, background, object position, and visual appearance.

---

## 3. Project Workflow

The project follows a staged machine learning workflow:

### A. Data Preparation
- image collection and organisation
- dataset splitting into train / validation / test sets
- preprocessing and standardisation
- data quality checks
- augmentation to improve robustness

### B. Model Development
- experimentation with transfer learning baselines
- custom CNN design and refinement
- training and validation comparison across model variants
- tuning for improved generalisation and stability

### C. Prediction Handling
- hierarchical interpretation of predictions
- adaptive confidence thresholding for uncertain inputs
- support for rejecting low-confidence outputs instead of forcing unreliable predictions

### D. Deployment Preparation
- export and conversion steps for TensorFlow Lite
- lightweight inference preparation for mobile or edge use cases

---

## 4. Key Features

- Structured train / validation / test dataset layout
- Fine-grained garlic and grape subclass labels
- Custom CNN experimentation
- Transfer learning benchmarking
- Hierarchical modelling concept
- Adaptive confidence thresholding for unknown or uncertain inputs
- TensorFlow Lite preparation for lightweight deployment

---

## 5. Repository Contents

- `Project_dataset_updated_split/` – main dataset split into train, val, and test
- `Project_dataset_updated_split_OT/` – additional dataset resources used in the project
- `Garlic_Grapes_Model.ipynb` – notebook containing the model development workflow
- `MLAI Mini Project.pdf` – supporting project report
- `README.md` – repository overview
- `requirements.txt` – environment and package setup commands

---

## 6. Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- pandas
- Matplotlib
- Pillow
- SciPy
- OpenCV
- scikit-learn
- Streamlit
- TensorFlow Lite

---

## 7. Environment Setup

The provided `requirements.txt` currently serves as an environment setup script rather than a standard pip requirements file. It includes installation commands for the main project dependencies and GPU-related setup.

Typical packages used in this project include TensorFlow, NumPy, pandas, Matplotlib, Pillow, SciPy, imagehash, splitfolders, seaborn, scikit-learn, OpenCV, and Streamlit.

---

## 8. Future Improvements

- replace the setup script with a standard installable `requirements.txt`
- add explicit training results and evaluation metrics to the README
- include sample predictions and confusion matrices
- document the hierarchical prediction logic in more detail
- package the inference workflow into a reproducible app demo
- extend unknown-class handling with clearer rejection criteria

---

## 9. Conclusion

This repository documents an end-to-end computer vision project for garlic and grape image classification. Beyond model training, the project also considers dataset structure, hierarchical label interpretation, confidence-aware prediction handling, and lightweight deployment preparation. The result is a more complete machine learning workflow than a basic single-model image classifier.
The final model is prepared for **mobile deployment**, enabling real-time image classification on-device.
