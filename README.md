🌿 Plant Disease Detection using Deep Learning

An AI-powered image classification system that detects plant diseases from leaf images using Convolutional Neural Networks (CNN). This project aims to support smart agriculture by enabling early disease identification.

📌 Overview

Plant diseases significantly reduce agricultural productivity. Early detection helps farmers take preventive measures and improve crop yield.
This project uses:
Deep Learning (CNN)
Image preprocessing & augmentation
Multi-class classification
Model evaluation & visualization
The trained model can classify plant leaves into healthy or diseased categories.

🧠 Technologies Used

Python
TensorFlow / Keras
NumPy
Pandas
Matplotlib
Seaborn
OpenCV
Scikit-learn

📊 Dataset

The dataset contains labeled images of plant leaves categorized into multiple classes such as:
Healthy
Early Blight
Late Blight
Leaf Mold
Bacterial Spot
Powdery Mildew
And more...
The images are preprocessed and resized to ensure uniform input for the CNN model.

🏋️ Model Training

The CNN model is trained using:
Optimizer: Adam
Loss Function: Categorical Crossentropy
Metric: Accuracy
Epochs: 30 (or as configured)

Example:

Python:
model.compile(
    optimizer='adam',
    loss='categorical_crossentropy',
    metrics=['accuracy']
)

history = model.fit(
    train_data,
    validation_data=val_data,
    epochs=30
)


📈 Model Evaluation

The model performance is evaluated using:
Training & Validation Accuracy
Loss Curves
Confusion Matrix
Classification Report
(Add your final accuracy here if available, e.g., Model achieved 94% validation accuracy)

🔍 Prediction on New Images

from tensorflow.keras.models import load_model
from tensorflow.keras.preprocessing import image
import numpy as np

model = load_model("plant_disease_model.h5")

img = image.load_img("leaf.jpg", target_size=(224,224))
img_array = image.img_to_array(img) / 255.0
img_array = np.expand_dims(img_array, axis=0)

prediction = model.predict(img_array)
print("Predicted Class:", prediction)

🚀 Future Improvements

🌐 Deploy as Web App (Flask / Streamlit)
📱 Mobile App Integration
🎥 Real-time Detection via Camera
🔬 Transfer Learning (ResNet, MobileNet)
⚡ Model Optimization for Edge Devices

