# Cat vs. Dog Image Classifier (CNN)

### Project Overview
This project involves building a **Convolutional Neural Network (CNN)** using **TensorFlow 2.0 and Keras** to classify images of cats and dogs. The primary goal was to achieve at least 63% accuracy (achieved: **[Insert Your Accuracy, e.g., 72%]**) while managing a relatively small training dataset through data augmentation techniques.

### Highlights
*   **Architecture:** Built a `Sequential` model utilizing a stack of `Conv2D` and `MaxPooling2D` layers for feature extraction, followed by `Dense` layers with `ReLU` and `Softmax/Sigmoid` activations.
*   **Data Augmentation:** Implemented `ImageDataGenerator` with random transformations (rotation, zoom, horizontal flip) to artificially expand the training set and reduce overfitting.
*   **Pipeline:** Developed a robust data pipeline using `flow_from_directory` to handle image decoding and tensor rescaling.

---

### Technical Methodology

#### **1. Data Engineering & Generators**
*   **Rescaling:** Converted image pixel values from $[0, 255]$ to floating-point tensors in the range $[0, 1]$.
*   **Generators:** Configured `train`, `validation`, and `test` generators.
*   **Test Handling:** Specifically configured the test generator with `shuffle=False` to ensure predictions matched the expected evaluation order.

#### **2. Model Architecture & Training**
*   **CNN Layers:** Structured multiple convolutional layers to identify patterns like edges, fur textures, and shapes.
*   **Optimization:** Compiled the model using the **Adam** optimizer and **Binary Crossentropy** loss.
*   **Training:** Trained the model using `model.fit`, monitoring both training and validation accuracy to detect potential variance/overfitting.

#### **3. Evaluation & Visualization**
*   **Performance Metrics:** Generated loss and accuracy graphs to visualize the learning curve.
*   **Probability Prediction:** Developed a prediction script that outputs the probability of an image being a dog or a cat, visualized with their respective images.

---

### View the Analysis: [View the Image Classifier Notebook](./fcc_cat_dog.ipynb)

### Tech Stack
*   **Framework:** TensorFlow 2.0, Keras
*   **Libraries:** NumPy, Matplotlib

*   **Techniques:** Convolutional Neural Networks (CNN), Data Augmentation, Image Preprocessing
