# EuroSAT Land Cover Classification using MobileNetV2
This project focuses on land cover classification using the EuroSAT dataset, which consists of satellite images captured by the Sentinel-2 satellite. The goal is to build an image classification model that can accurately categorize land types into one of 10 classes, including:

Industrial buildings
Residential areas
Forests
Farmland
Rivers and lakes
Highways
... and more.
Accurate land cover classification is important for urban planning, environmental monitoring, and disaster management. By leveraging a pretrained MobileNetV2 model and fine-tuning it on the EuroSAT dataset, we aim to develop a lightweight and efficient classifier for remote sensing applications.
## Dataset
The dataset used is EuroSAT RGB, which consists of satellite images categorized into 10 classes.
Images are resized to 224x224 and normalized.
The dataset is split into 80% training and 20% validation.

## Model Architecture
Pretrained MobileNetV2 is fine-tuned for this classification task.
The last classification layer is replaced to match the number of classes (10).
Training is done using:
Adam optimizer
Cross-entropy loss
Batch size: 16
Learning rate: 0.001
Number of epochs: 10
