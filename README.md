# EuroSAT Land Cover Classification using MobileNetV2
This project focuses on land cover classification using the EuroSAT dataset, which consists of satellite images captured by the Sentinel-2 satellite. The goal is to build an image classification model that can accurately categorize land types into one of 10 classes, including:

- Industrial buildings
- Residential areas
- Forests
- Farmland
- Rivers and lakes
- Highways
... and more.
Accurate land cover classification is important for urban planning, environmental monitoring, and disaster management. By leveraging a pretrained MobileNetV2 model and fine-tuning it on the EuroSAT dataset, we aim to develop a lightweight and efficient classifier for remote sensing applications.
## Dataset
The dataset used is EuroSAT RGB, which consists of satellite images categorized into 10 classes.
Images are resized to 224x224 and normalized.
The dataset is split into 80% training and 20% validation.

## Model Architecture
- Pretrained MobileNetV2 is fine-tuned for this classification task.
- The last classification layer is replaced to match the number of classes (10).
- Training is done using:
- Adam optimizer
- Cross-entropy loss
- Batch size: 16
- Learning rate: 0.001
- Number of epochs: 10

## Classification Report

                       | Class                   | Precision | Recall | F1-Score | Support |
|-------------------------|-----------|--------|----------|---------|
| **AnnualCrop**          | 0.92      | 0.98   | 0.95     | 562     |
| **Forest**              | 0.99      | 0.99   | 0.99     | 583     |
| **HerbaceousVegetation**| 0.97      | 0.94   | 0.95     | 595     |
| **Highway**             | 0.96      | 0.99   | 0.97     | 489     |
| **Industrial**          | 0.98      | 0.97   | 0.97     | 515     |
| **Pasture**             | 0.98      | 0.94   | 0.96     | 448     |
| **PermanentCrop**       | 0.91      | 0.97   | 0.94     | 506     |
| **Residential**         | 1.00      | 0.97   | 0.98     | 626     |
| **River**              | 0.99      | 0.96   | 0.98     | 468     |
| **SeaLake**            | 1.00      | 0.98   | 0.99     | 608     |

**Overall Accuracy:** 🎯 **97%**  
**Macro Average:** 0.97 (Precision) | 0.97 (Recall) | 0.97 (F1-Score)  
**Weighted Average:** 0.97 (Precision) | 0.97 (Recall) | 0.97 (F1-Score)

<img width="819" alt="image" src="https://github.com/user-attachments/assets/9c9b922f-d0d8-43c9-87d9-2991181099f2" />
