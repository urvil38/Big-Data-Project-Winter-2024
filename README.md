## Pneumonia Detection

Our project focuses on creating a robust and reliable system designed to classify X-ray images of lungs into distinct classes, including COVID-19, bacterial pneumonia, viral pneumonia, lung opacity, and normal cases. The data for this project is organized into three key categories: training, validation, and test sets, ensuring comprehensive learning and evaluation phases. This endeavor aims to significantly enhance healthcare delivery and improve patient outcomes by leveraging a dataset partitioned into training, validation, and test sets. By distinguishing between these conditions effectively, our project seeks to enhance medical diagnostic processes significantly.

### Problem Statement

The project is structured around two core objectives:

1. **Data Preparation**: Compiling a comprehensive dataset of labeled X-ray images. This involves collecting, preprocessing, and augmenting images to ensure a diverse and representative dataset for training our models.

2. **Model Training and Evaluation**: Training and fine-tuning ResNet and EfficientNet models on our dataset. The goal is to compare these models in terms of accuracy, efficiency, and their ability to generalize from training data to unseen X-ray images.

### Challenges

- **Variability in X-ray Images**: Addressing differences in image quality, patient positioning, and visible artifacts to ensure consistent model performance.
- **Class Imbalance**: Managing uneven distribution of classes within the dataset, particularly the lower prevalence of COVID-19 cases, to avoid model bias.

### Dataset Specifications

Each class has over 700 X-ray images:

| Column              | Details                                                                              |
|---------------------|--------------------------------------------------------------------------------------|
| Covid-19            | Lungs infected with the covid 19 virus                                               |
| Bacterial Pneumonia | Pneumonia-infected lungs given from various bacteria                                 |
| Viral Pneumonia     | Pneumonia-infected lungs given from viruses                                          |
| Lung Opacity        | Other lung diseases that are not Pneumonia                                           |
| Normal              | Normal healthy lungs                                                                 |

### Data Preprocessing

Our preprocessing workflow involves resizing images to a consistent dimension, normalizing pixel values, and applying data augmentation (e.g., rotation, flipping) to enhance model training.

### Comparison Approaches

- **ResNet**: We will utilize the ResNet architecture, known for its deep residual learning framework, to capture complex patterns in the data.
 
- **EfficientNet**: EfficientNet will be used for its scalable architecture, allowing us to efficiently manage model complexity and computational cost.

### Key Research Questions

1. **ResNet vs. EfficientNet Performance**: How do ResNet and EfficientNet compare in terms of accuracy and computational efficiency for pneumonia detection in our dataset?
   
2. **Preprocessing and Augmentation Impact**: Which preprocessing and data augmentation techniques are most effective for each model in improving generalization to new images?

3. **Class Imbalance Mitigation**: What strategies are most effective in balancing the class distribution for both models, ensuring accurate detection across all pneumonia types?

By addressing these questions, our team aims to develop a reliable and efficient tool for pneumonia detection, offering valuable support to healthcare professionals.
