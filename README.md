**Project Overview**
The primary goal of this project is to develop an Explainable AI (XAI) system for detecting skin cancer. By combining Deep Learning models with transparency tools like LIME, the system doesn't just provide a diagnosis (benign or malignant) but also highlights the specific visual features of a skin lesion that led to that decision, helping clinicians trust the AI's output.

**File Descriptions**

**cnn.ipynb**: This is the core technical notebook. It handles the Data Preprocessing (including resizing, normalization, and augmentation), model training, and evaluation. It contains the logic for the CNN architecture used to classify the skin images.

**main.py**: The entry point for the application. This file integrates the trained model with the user interface, orchestrating the flow between user input and model prediction.

**gui.py**: Contains the code for the Graphical User Interface. It manages the layout, buttons, and display areas where the user interacts with the system.

model.h5 / model.keras: The saved, pre-trained weights of your CNN model, which are loaded by the GUI to perform real-time predictions.

**GUI Functionality**
The GUI serves as the bridge between the complex AI model and the end-user. Its main functions include:
1. Image Upload: Allows users to select and upload dermatoscopic images of skin lesions.
2. Classification: At the click of a button, it processes the image through the CNN and displays whether the lesion is likely Benign or Malignant.
3. Explainability Display: It generates and shows a LIME explanation map, overlaying a heatmap on the original image to show which parts of the lesion influenced the model's prediction the most.
4. Confidence Scoring: Provides a percentage or probability score to indicate how certain the model is about its diagnosis.
