# Garlic vs Grape Image Classification System  
**Custom CNN + Transfer Learning + Hyperparameter Optimization + TensorFlow Lite Deployment**

---

## 1. Project Introduction & Objectives

This project develops a deep learning-based image classification pipeline to accurately distinguish between **garlic** and **grape** images under varied real-world conditions.

The objective was to design and evaluate a **complete computer vision workflow**, covering:

1. Dataset preparation and preprocessing  
2. Transfer learning benchmarking using pretrained CNNs  
3. Custom CNN architecture development  
4. Hyperparameter tuning and optimisation  
5. Model comparison and selection  
6. TensorFlow Lite conversion for on-device inference  

The final model is prepared for **mobile deployment**, enabling real-time image classification on-device.

---

## 2. System Architecture Overview

The project follows a structured experimental workflow:

### **Section A: Dataset Engineering**

A curated dataset of garlic and grape images was constructed and standardised.

Key processes include:

- Image resizing and normalization  
- RGB standardisation  
- Data augmentation (rotation, flipping, etc.)  
- Train / validation / test splitting  
- Basic data cleaning and integrity checks  

The dataset was designed to introduce variability in:

- Lighting conditions  
- Background clutter  
- Object positioning  
- Partial occlusion  

---

### **Section B: Transfer Learning Benchmarking**

Pretrained convolutional neural networks were evaluated as baseline models:

- **InceptionV3**  
- **MobileNetV2**  
- **ResNet50V2**

Each model was initialised with ImageNet weights and adapted for binary classification.

#### Transfer Learning Strategy

- Frozen feature extractor during initial training  
- Custom classification head with:
  - Global Average Pooling  
  - Dense layers  
  - Dropout for regularisation  
- Partial layer unfreezing for fine-tuning  
- Reduced learning rate during fine-tuning  

This phase established strong baseline performance before exploring custom architectures.

---

### **Section C: Custom CNN Architecture Development**

A convolutional neural network was developed from scratch through iterative experimentation.

#### Architectural Components

- Conv2D layers with ReLU activation  
- Batch Normalization  
- MaxPooling layers  
- Dropout layers for regularisation  
- Fully connected dense layers  
- Sigmoid output layer for binary classification  

Multiple architectures were tested to address:

- Underfitting  
- Overfitting  
- Training instability  
- Generalisation performance  

Models were evaluated based on:

- Validation accuracy  
- Generalisation gap  
- Convergence behaviour  
- Model complexity  

---

## 3. Hyperparameter Optimization Strategy

A consistent training configuration was used across experiments:

| Hyperparameter | Setting |
|---------------|--------|
| Optimizer | Adam |
| Learning Rate | 1e-4 |
| Batch Size | 32 |
| Loss Function | Binary Crossentropy |
| Initialization | He Normal |

### Training Optimisation Techniques

- **ReduceLROnPlateau** – dynamically lowers learning rate  
- **Early Stopping** – prevents overfitting  
- **Model Checkpointing** – saves best-performing model  

---

## 4. Model Comparison & Selection

Models were compared based on:

- Validation and test accuracy  
- Overfitting behaviour  
- Model size and efficiency  
- Inference speed  

The selected model achieved a good balance between **accuracy, stability, and efficiency**, making it suitable for deployment.

---

## 5. TensorFlow Lite Conversion & Deployment

The final model was converted to **TensorFlow Lite (TFLite)** for lightweight deployment.

### Conversion Process

- Export trained model  
- Convert to TFLite format  
- Validate inference outputs  
- Optimise for reduced size  

### Deployment Use Case

- Real-time image classification  
- On-device inference (no internet required)  
- Low-latency predictions  
- Lightweight storage footprint  

---

## 6. Key Highlights

- End-to-end ML pipeline from data preparation to deployment  
- Benchmarking of pretrained models vs custom CNN  
- Structured hyperparameter tuning approach  
- Deployment-ready model using TensorFlow Lite  

---

## 7. Technologies Used

- Python  
- TensorFlow / Keras  
- NumPy / Matplotlib  
- OpenCV / PIL  
- TensorFlow Lite  

---

## 8. Future Improvements

- Model quantisation for faster inference  
- Multi-class classification (more food categories)  
- Larger and more diverse dataset  
- Integration into a full mobile application  

---

## 9. Conclusion

This project demonstrates a complete machine learning workflow for image classification, from dataset preparation to deployment. By combining transfer learning, custom CNN development, and structured experimentation, the system achieves reliable classification of garlic and grape images while remaining suitable for lightweight deployment.
- **InceptionV3**
- **MobileNetV2**
- **ResNet50V2**

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
