# ExplainCrop AI

[![Python](https://img.shields.io/badge/Python-3.x-blue)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)](https://www.tensorflow.org/)
[![Intel oneAPI](https://img.shields.io/badge/Intel-oneAPI-blue)](https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html)

## Project Overview

ExplainCrop AI is an advanced computer vision system developed to identify plants and weeds from images and provide actionable agricultural insights. It combines deep learning-based classification with Explainable AI techniques to ensure transparency and interpretability in model predictions.

The project utilizes **MobileNetV2** for transfer learning to classify plant species such as *Celosia Argentea*, *Crowfoot Grass*, and *Purple Chloris*. Additionally, Grad-CAM (Gradient-weighted Class Activation Mapping) is integrated to highlight regions of images that contributed most to the model’s predictions. The system also includes a decision advisory module that informs users about plant risk levels and recommended actions.

---

## Features

- Image-based classification of plants and weeds.  
- Transfer learning using MobileNetV2 for efficient and accurate predictions.  
- Explainable AI via Grad-CAM visualizations to interpret model decisions.  
- Smart advisory system providing risk level and recommended action.  
- Optimized data processing pipeline for fast and reproducible training.  

---

## How the System Works

1. User uploads an image of a plant or weed.  
2. The model predicts the class of the plant.  
3. The system determines:
   - Whether it is a weed or useful plant.  
   - The associated risk level.  
   - Recommended actions based on the classification.  
4. Grad-CAM generates a visual heatmap highlighting the regions responsible for the prediction.

---

## Explainable AI – Grad-CAM

Grad-CAM (Gradient-weighted Class Activation Mapping) is employed to enhance the interpretability of the model. It generates heatmaps that indicate the regions in an image most influential in determining the predicted class. This improves trust in the model and helps identify potential misclassifications.

**Benefits:**

- Enhances user confidence in predictions.  
- Provides visual insights into which parts of the plant the model focuses on.  
- Useful for debugging incorrect predictions.  
- Bridges the gap between AI predictions and actionable agricultural decisions.  

### Original vs Grad-CAM Visualization

<table>
  <tr>
    <td><b>Original Image</b></td>
    <td><b>Grad-CAM Heatmap</b></td>
  </tr>
  <tr>
    <td><img src="images/sample.jpg" width="300"></td>
    <td><img src="images/gradcam_result.jpg" width="300"></td>
  </tr>
</table>

**Interpretation:**  
- Red indicates regions with high influence on the prediction.  
- Yellow indicates medium influence.  
- Blue indicates low influence.  

---

## Technology Stack

- Python 3.x  
- TensorFlow / Keras for deep learning  
- OpenCV for image processing  
- NumPy for numerical computations  
- Matplotlib for plotting and visualization  
- Intel oneAPI (oneDNN + oneDAL via sklearnex) for performance optimization  

---

## Intel oneAPI Optimization

The project leverages Intel oneAPI to accelerate computations:

- TensorFlow is optimized with **oneDNN** for faster model inference.  
- Scikit-learn operations are enhanced using **oneDAL (sklearnex)** for improved training performance.  

---

## Sample Output

The system provides:

- Predicted class with confidence score.  
- Risk assessment (low or high).  
- Recommended actions for the user.  
- Grad-CAM heatmap to interpret model focus.

### Sample Input
<img src="images/sample.jpg" width="400">

### Prediction Output
<img src="images/prediction.png" width="400">

### Grad-CAM Heatmap
<img src="images/gradcam_result.jpg" width="400">

---

## Model Performance

- Achieved approximately 95% validation accuracy.  
- Consistent classification performance across all plant and weed classes.  

---

## Objective

The primary goal of ExplainCrop AI is to assist farmers and agricultural professionals in identifying harmful weeds and beneficial plants while providing explainable and actionable insights to support informed decision-making.

---

## Installation

Clone the repository and install required dependencies:

```bash
pip install -r requirements.txt
