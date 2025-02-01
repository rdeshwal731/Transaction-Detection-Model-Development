# Transaction-Detection-Model-Development
## Objective

Developing and training a machine learning model that detects and classifies bank transactions (e.g., UPI, NEFT, RTGS) from the provided dataset of images. The goal is to create a robust solution that achieves at least 90% accuracy on the test data.

## Task Details

### Dataset

You can access it using the following link:
[Dataset Link](https://drive.google.com/file/d/1-wKCz6xqpHz3g4LQHfPl3pyzpmrPfgt4/view)

## Overview
This project implements a binary image classification model to determine whether a transaction is categorized as "Yes" or "No." It utilizes TensorFlow's EfficientNetB0 and VGG19 architectures for training, validation, and testing.

## Features
- Downloads and preprocesses transaction image data.
- Splits images into training, validation, and test sets.
- Uses VGG19 for feature extraction and fine-tuning.
- Implements data augmentation to improve model generalization.
- Includes training with early stopping and model checkpointing.
- Converts and saves the trained model to ONNX format for interoperability.

## Installation
Ensure you have the required dependencies installed:

```bash
pip install tensorflow onnx gdown tf2onnx keras2onnx
```

## Usage
1. **Download and Extract Dataset**
   - The script downloads a dataset from Google Drive and extracts it.
2. **Data Splitting**
   - Images are split into `train`, `val`, and `test` sets.
3. **Model Training**
   - A VGG19-based model is trained on the dataset.
   - Early stopping and checkpointing are used to optimize training.
4. **Model Evaluation**
   - The model is tested on unseen images to assess accuracy.
5. **ONNX Model Conversion**
   - The trained model is converted to ONNX format for deployment.

## Output
- The best model is saved as `best_model.h5`.
- Training performance plots are generated.
- The final model is converted and saved as `model.onnx`, which can be downloaded from [this link](https://drive.google.com/file/d/1ad85_x27DKhdr0ZEahr2MZ74vfg73JLd/view?usp=sharing).

## Notes
- Modify the dataset URL if necessary.
- Adjust hyperparameters (e.g., epochs, batch size) in the `train_efficientnet_from_folders` function to optimize performance.

## Author
Developed using Google Colab and TensorFlow.

## License
This project is licensed under the MIT License.

