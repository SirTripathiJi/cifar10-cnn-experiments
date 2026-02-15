# cifar10-cnn-experiments
# CIFAR-10 CNN Experiments

Convolutional Neural Network (CNN) baseline trained on the CIFAR-10 dataset with structured experimentation and training curve analysis.

---

## 📌 Overview

This repository presents a CNN baseline trained on CIFAR-10 as part of a controlled experimentation study. The objective was to evaluate:

- Training dynamics  
- Generalization behavior  
- Impact of regularization  
- Optimization strategies under structured modifications  

The emphasis of this project is disciplined experimentation and analytical reasoning — not just final accuracy.

---

## 📂 Dataset

| Attribute | Details |
|-----------|----------|
| Dataset | CIFAR-10 |
| Classes | 10 object categories |
| Image Size | 32 × 32 RGB |
| Training Samples | 5,000–10,000 (subset constraint) |
| Validation Split | 10% |
| Test Set | Standard CIFAR-10 test split |

---

## 🏗 Model Architecture

Deep convolutional architecture with progressive feature extraction:

- Convolutional blocks with `3×3` kernels  
- Batch Normalization after each convolution  
- MaxPooling layers for spatial downsampling  
- Dropout for regularization  
- L2 weight decay  
- Final Dense layer with Softmax activation  

**Total Parameters:** ~1.2M  

---

## ⚙️ Training Configuration

| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Learning Rate | 0.0005 |
| Loss Function | Categorical Crossentropy |
| Batch Size | 64 |
| Epochs | 150 (with Early Stopping) |
| LR Scheduler | ReduceLROnPlateau |
| Regularization | L2 + Dropout |

### Data Augmentation
- Rotation  
- Width shift  
- Height shift  
- Zoom  
- Shear  

---

## 📊 Baseline Results

| Metric | Value |
|--------|--------|
| Validation Accuracy | ~91% |
| Test Accuracy | ~90% |
| Test Loss | ~0.43 |

Training converged smoothly with minimal train–validation divergence, indicating effective regularization and stable optimization.

---

## 📈 Training Curve Analysis

- Training and validation loss decrease consistently over epochs  
- Accuracy steadily improves and stabilizes  
- Small generalization gap indicates controlled overfitting  
- Learning rate scheduling improved late-stage convergence  
- Early stopping restored best-performing weights  

The model demonstrates stable optimization behavior.

---

## 🔬 Controlled Experiments

The following variations were evaluated:

1. Learning rate modification  
2. Dropout configuration adjustments  
3. Regularization strength tuning  
4. Data augmentation impact  

### Key Observations

- Higher learning rates improved early convergence but reduced stability  
- Removing dropout increased overfitting  
- L2 regularization reduced generalization gap  
- Data augmentation improved robustness across classes  

---

## 🔁 Reproducibility

Implemented in **TensorFlow / Keras**.

The notebook includes:
- Full preprocessing pipeline  
- Model definition  
- Training curves  
- Evaluation metrics  
- Experiment comparisons  

All results are reproducible using the provided notebook.

---

## ✅ Conclusion

A well-regularized CNN baseline combined with structured experimentation and learning rate control achieves strong generalization performance (~90% test accuracy) on CIFAR-10 without requiring complex architectures.

This work emphasizes:
- Structured experimentation  
- Analytical interpretation  
- Controlled modification analysis  
- Clear training behavior evaluation  

---

