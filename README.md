# Grapes vs Onion Image Classification System  
**Custom CNN + Transfer Learning + Hyperparameter Optimization + TensorFlow Lite Deployment**

---

## 1. Project Introduction & Objectives

This project develops a production-ready deep learning pipeline capable of accurately distinguishing between **Peach** and **Onion** images under real-world conditions.

The objective was not merely to build a classifier, but to engineer a **fully optimized computer vision system** that includes:

1. **Dataset construction and preprocessing**
2. **Transfer learning benchmarking (Pretrained CNNs)**
3. **Custom CNN architecture development**
4. **Systematic hyperparameter tuning**
5. **Model comparison and selection**
6. **TensorFlow Lite deployment for mobile inference**

The final model is deployed into a **mobile application** using TensorFlow Lite, enabling real-time classification on-device.

---

## 2. System Architecture Overview

The project follows a structured experimental progression:

### **Section A: Dataset Engineering**

A curated dataset of Peach and Onion images was constructed and standardized.

Key processes include:

- Image resizing and normalization
- Format conversion and RGB standardization
- Data augmentation for robustness
- Train / Validation / Test splitting
- Corruption filtering and integrity verification

The dataset was designed to simulate real-world variability in:

- Lighting conditions
- Background clutter
- Object positioning
- Partial occlusion

---

### **Section B: Transfer Learning Benchmarking**

State-of-the-art pretrained architectures were evaluated as baselines:

- **MobileNetV2**
- **ResNet50**
- **EfficientNetB0**

Each model utilized ImageNet pretrained weights and was fine-tuned for binary classification.

#### Transfer Learning Strategy

- Frozen feature extractor initialization
- Custom classification head with:
  - Global Average Pooling
  - Dense layers with L2 regularization
  - Dropout for overfitting control
- Selective layer unfreezing
- Reduced learning rate during fine-tuning

This phase established high-performance benchmarks before developing custom architectures.

---

### **Section C: Custom CNN Architecture Development**

A Convolutional Neural Network was developed from scratch through iterative experimentation.

#### Architectural Components

- Stacked Conv2D layers with ReLU activation
- Batch Normalization for stability
- MaxPooling for spatial compression
- Dropout for regularization
- Fully connected dense head
- Softmax output layer

Multiple versions were tested to overcome:

- Feature underfitting
- Over-parameterization
- Training instability
- Validation performance plateaus

Each version was evaluated on:

- Validation Accuracy
- Generalization Gap
- Convergence Speed
- Parameter Efficiency

---

## 3. Hyperparameter Optimization Strategy

To ensure fair comparison across all models, a controlled hyperparameter framework was implemented.

| Hyperparameter | Final Setting | Rationale |
|---------------|--------------|-----------|
| Optimizer | Adam | Adaptive learning suitable for CNN training |
| Learning Rate | 1e-4 (initial) | Stability + convergence balance |
| Batch Size | 32 | Optimized for GPU memory and generalization |
| Loss Function | Binary Crossentropy | Appropriate for binary classification |
| Initialization | He Normal | Designed for ReLU-based networks |

---

### Dynamic Optimization Mechanisms

To enhance convergence reliability:

- **ReduceLROnPlateau**
  - Automatically lowers learning rate upon validation stagnation
- **Early Stopping**
  - Prevents overfitting and restores best weights
- **Model Checkpointing**
  - Preserves highest validation accuracy model

---

## 4. Model Comparison & Selection

Models were compared across multiple dimensions:

- **Validation Accuracy**
- **Test Accuracy**
- **Inference Speed**
- **Model Size**
- **Parameter Count**
- **Overfitting Behavior**

The best-performing architecture demonstrated:

- High confident accuracy
- Stable convergence
- Low inference latency
- Efficient parameter usage

This model was selected for deployment.

---

## 5. TensorFlow Lite Conversion & Mobile Deployment

The selected model was converted to **TensorFlow Lite (TFLite)** for edge-device deployment.

### Conversion Process

- SavedModel export
- Post-training optimization
- TFLite conversion
- Model size compression
- Float32 compatibility validation

### Mobile App Integration

The TFLite model was integrated into a mobile application enabling:

- Real-time camera inference
- On-device classification
- Low-latency prediction
- Lightweight storage footprint

This ensures the system functions without requiring cloud connectivity.

---

## 6. Key Engineering Highlights

### I. End-to-End ML Pipeline
Complete lifecycle from dataset creation to mobile deployment.

### II. Comparative Architecture Study
Systematic benchmarking of pretrained vs custom CNN models.

### III. Controlled Hyperparameter Framework
Ensured fair experimental comparison across architectures.

### IV. Deployment-Ready Optimization
Model optimized for real-world mobile constraints.

---

## 7. Technologies Used

- Python
- TensorFlow / Keras
- NumPy / Matplotlib
- OpenCV / PIL
- TensorFlow Lite
- Android / Flutter (Mobile Integration)

---

## 8. Future Improvements

- Quantization-aware training
- Confidence threshold rejection system
- Multi-class extension (e.g., fruit vs vegetable classifier)
- Edge TPU optimization

---

## 9. Conclusion

This project demonstrates a full-stack machine learning workflow, progressing from raw dataset engineering to production-level mobile deployment. Through systematic experimentation, transfer learning benchmarking, custom CNN development, and hyperparameter optimization, the final system achieves reliable and efficient Peach vs Onion classification in real-world environments.
