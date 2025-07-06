# Garbage Classification with Deep Learning

This project involves developing an AI-based system that can automatically classify images of garbage into categories like plastic, metal, paper, etc. The aim is to make waste segregation more intelligent and efficient, promoting better recycling and environmental practices.

## What's Inside

- A deep learning model built using EfficientNetV2B2
- Custom layers added on top for effective trash classification
- A Gradio interface for quick, real-time image predictions
- Visual evaluation through confusion matrix and heatmaps
- Clean, easy-to-understand, and extendable codebase

## Tech Stack

- Python
- TensorFlow / Keras
- EfficientNetV2B2 (used via transfer learning)
- scikit-learn
- matplotlib and seaborn for visualizations
- Gradio for the interactive frontend
- Jupyter Notebook for experiments and prototyping

## Dataset

The model was trained on a labeled dataset of various types of waste.

- All images were resized to 124×124 pixels
- Dataset split: 80% training, 20% validation
- Loaded using TensorFlow’s image_dataset_from_directory()

## How It Works

### 1. Load and Prepare the Data
- Images are resized, batched, shuffled
- Dataset is cached and prefetched for performance

### 2. Build the Model
- EfficientNetV2B2 serves as the base model
- Additional layers like Dropout and Dense are added for classification

### 3. Train the Model
- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Callbacks: EarlyStopping and ReduceLROnPlateau for better training control

### 4. Evaluate Performance
- Generate a confusion matrix and classification report
- Plot training history and performance metrics

### 5. Deploy the Model
- Use a Gradio web app to serve predictions in real time through a simple UI
