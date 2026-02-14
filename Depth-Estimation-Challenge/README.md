# Depth Estimation Challenge
**🏆 Ranked 4th out of 45 Teams**

## Project Overview
This project was part of a deep learning competition focused on **Monocular Depth Estimation**. The objective was to develop a model capable of estimating depth maps from single RGB images. This task is critical for applications in autonomous driving, robotics, and augmented reality.



## 🛠️ Technical Approach
The solution utilizes a specialized encoder-decoder architecture designed for image-to-image translation tasks.

### 1. Model Architecture
* **Architecture:** `U-Net`
* **Backbone (Encoder):** `ResNet-34` pre-trained on ImageNet.
* **Decoder:** Standard U-Net decoder with sigmoid activation for normalized depth output.
* **Framework:** `segmentation-models-pytorch` (SMP).



### 2. Training Pipeline
* **Preprocessing:**
    * Images resized to **256x256**.
    * RGB normalization and transposition to PyTorch tensor format.
* **Loss Function:** `MSELoss` (Mean Squared Error) to minimize pixel-wise depth differences.
* **Optimization:**
    * **Optimizer:** `Adam` with a learning rate of `0.0001`.
    * **Epochs:** 15.
    * **Validation:** Monitored RMSE (Root Mean Squared Error) of mean intensities to align with competition scoring.

## 📈 Performance
* **Best Validation RMSE:** **17.33898**.
* **Leaderboard:** Ranked **4/45** in the private competition.

## 📂 File Structure
* `Image_Depth_Estimation.ipynb`: Full training script including data splitting, model definition, and inference.
* `requirements.txt`: Dependencies for environment reproduction.
