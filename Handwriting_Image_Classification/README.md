# DLP Image Classification for Handwriting
**🏆 Ranked 1st out of 110 Teams**

## Project Overview
This project was developed for the **Deep Learning Practice** course as part of the **IIT Madras BS in Data Science & Applications** program. The goal was to build a robust image classification model to recognize handwritten numerals from a provided dataset.

## 🛠️ Technical Approach
The solution leverages a Transfer Learning approach with a focus on high-resolution processing and data augmentation to handle variances in handwriting styles.

### 1. Model Architecture
* **Base Model:** EfficientNet-B1 (Pre-trained on ImageNet).
* **Customization:** The final fully connected layer was modified to output 10 classes (digits 0-9).
* **Loss Function:** CrossEntropyLoss with Label Smoothing (0.1) to improve generalization.

### 2. Training Strategy
* **Resolution:** Images were resized to 256x256 for better feature extraction.
* **Augmentation:** Applied random rotations (15°), shifts (10%), and scaling (0.85–1.15x) to mimic human handwriting variability.
* **Optimization:** * **Optimizer:** Adam with a learning rate of 0.0005.
    * **Scheduler:** CosineAnnealingWarmRestarts over 15 epochs to find the optimal global minimum.

## 📈 Performance
* **Training Accuracy:** Achieved ~99.7% on the training set.
* **Leaderboard:** Ranked 1/110 in the competition.

## 📂 File Structure
* `handwriting-image-classification.ipynb`: The main training and inference pipeline.
* `requirements.txt`: List of dependencies required to run the notebook.
