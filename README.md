# Eye Disease Image Classification with Convolutional Neural Network (CNN) Approaches

## Overview
Early detection of ocular diseases such as cataracts and glaucoma can significantly improve prognosis. Automated detection algorithms leverage deep learning approaches and have gained traction in ophthalmic classification. Convolutional neural networks (CNN) have demonstrated impressive accuracy and potential to streamline diagnosis, reduce inconsistencies, and optimize healthcare resources. Challenges remain in scaling models for clinical integration and commercialisation. 

This repo explores three CNN model architectures in image classification – Simple CNN architecture, ResNet50, VGG-16

### Workflow of all model building approaches 
<img width="444" height="176" alt="image" src="https://github.com/user-attachments/assets/6d54dee4-8956-4f28-bf3a-757eeac61ae5" />

## Methods
**All models were developed and evaluated in Python (TensorFlow, Keras, NumPy, scikit-learn) within Google Colab, implementing a full machine learning workflow including preprocessing, model training, validation, hyperparameter tuning and performance evaluation.**

- **Dataset:** 501 retinal fundoscopic images
    - 300 no disease
    - 100 cataracts
    - 101 glaucoma 
- **Training strategy:** 70% training data, 15% validation data, 15% testing data
-	**Model evaluations:** model performance metrics used included accuracy, recall (sensitivity), F1-scores and specificity. These metrics were calculated from values determined from confusion matrices.

## Model architectures
<img width="452" height="101" alt="image" src="https://github.com/user-attachments/assets/dfa3635a-a4a4-458f-8714-d8982cf04536" />

-	**Simple CNN architecture:** lightweight sequential model designed for efficient training on limited medical datasets, incorporating convolutional feature extraction, max-pooling, dropout regularisation and softmax classification.
-	**ResNet50:** pre-trained model allows for learned features from a large diverse dataset to be applied for this classification.
-	**VGG-16:** pre-trained detection and classification algorithm popularised for its simplistic and uniform configurations of sequential convolutional and pooling layers.

## Highlights 
-	VGG-16 achieved the strongest performance (cross-validation accuracy: 72.4%), demonstrating the value of transfer learning for small biomedical datasets
-	ResNet50’s complex architecture risked overfitting to smaller, imbalanced datasets, hence several finetuning methods attempted to mitigate this (e.g. unfreezing layers, altering learning rates, L2 regularisation, dropout rates).
-	Simple CNN model stagnated in training and validation accuracies, therefore struggling extracting meaningful patterns from the dataset 

## Considerations
- Glaucoma classification suffered poorer metrics due to the inherent small and imbalanced nature of the image dataset.
- Model diagnostic abilities may ultimately depend on quantity and quality of image datasets used in training 
-	Future directions to optimise similar detection algorithms can revolutionise early detection of cataracts and glaucoma, which currently serve as two significant contributors to global blindness.



