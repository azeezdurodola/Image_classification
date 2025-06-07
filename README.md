# Animal Image Classification – GoogLeNet vs AlexNet

This project explores the use of **transfer learning** to classify animal images using two well-established convolutional neural networks (CNNs): **GoogLeNet** and **AlexNet**.  
The work was completed in MATLAB as part of my MSc in Artificial Intelligence and Data Science.

---

## Project Overview

- **Goal**: Compare GoogLeNet and AlexNet for wildlife image classification using transfer learning.
- **Dataset**: [Animals 10 Dataset on Kaggle](https://www.kaggle.com/alessiocorrado99/animals10)
- **Tools**: MATLAB, Deep Learning Toolbox
- **Accuracy**:  
  - GoogLeNet: 97.72%  
  - AlexNet: 97.85%

---

## Real-World Problem

Scientists use wildlife camera traps to monitor animal activity. These cameras generate thousands of images that require manual labeling — a time-consuming process. This project aims to automate animal recognition in those images, helping conservationists quickly sort and analyze large datasets.

---

## Deep Learning Strategy

- **Approach**: Transfer Learning
- **Why**: Enables high accuracy with small and imbalanced datasets
- **Models used**: GoogLeNet and AlexNet (pretrained on ImageNet)
- **Modifications**: Final layers adjusted for 10 animal classes using fully connected layers, softmax, and classification output

---

## Dataset and Preprocessing

- **Dataset**: 10 animal categories including dog, cat, cow, elephant, spider, etc.
- **Image Input Size**: Resized to 224x224 pixels
- **Splitting**: 70% training, 30% validation
- **Tools**: `imageDatastore` and `augmentedImageDatastore` for automatic labeling and resizing

---

## Training Configuration

- Epochs: 6  
- Batch Size: 32  
- Learning Rate: 0.0001  
- Optimizer: SGDM  
- Validation: Every 10 iterations

---

## Results

| Model     | Accuracy (%) | Training Time | Structure  | Notes                          |
|-----------|---------------|----------------|------------|-------------------------------|
| GoogLeNet | 97.72         | Moderate       | Deeper     | Better for complex features  |
| AlexNet   | **97.85**     | Faster         | Shallower  | Easier to train, more robust |

- Both models showed strong generalization and minimal overfitting.
- Confusion matrices revealed high performance across all classes, with AlexNet slightly outperforming GoogLeNet on underrepresented classes like "Cow".

---

## Visuals

- Confusion matrices  
- Training accuracy curves  
*(See `visuals/` folder for graphs and screenshots)*

---

## Key Learnings

- Simpler models like AlexNet can outperform deeper ones when datasets are balanced and well-preprocessed.
- Transfer learning is highly effective for limited-data scenarios.
- MATLAB’s toolbox made model customization and image handling efficient.

---

## Future Improvements

- Apply **data augmentation** (flip, rotate, brightness)
- Test on **external datasets** for generalizability
- Use **class weights** to better handle imbalanced classes
- Explore **Grad-CAM** for model explainability
- Try **ensemble methods** for improved performance

---



