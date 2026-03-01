🌿 Plant Disease Detection using Deep Learning
An AI-based image classification project that detects plant diseases from leaf images using Convolutional Neural Networks (CNN). This system helps in early identification of plant diseases to support farmers and agricultural researchers.
📌 Project Overview
Plant diseases significantly impact crop yield and food production. This project leverages Deep Learning (CNN) to classify plant leaf images into healthy or diseased categories.
The model is trained on a labeled plant leaf dataset and can predict disease types with high accuracy.
🚀 Features
✅ Image preprocessing & normalization
✅ Data augmentation for better generalization
✅ CNN-based deep learning model
✅ Multi-class disease classification
✅ Model evaluation using accuracy & loss metrics
✅ Prediction on custom leaf images
🧠 Tech Stack
Python
TensorFlow / Keras
NumPy
Pandas
Matplotlib / Seaborn
Scikit-learn
OpenCV
📂 Project Structure
Copy code

Plant-Diseases-Detection/
│
├── dataset/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── model/
│   └── plant_disease_model.h5
│
├── notebooks/
│   └── plant_disease_detection.ipynb
│
├── requirements.txt
└── README.md
📊 Dataset
The model is trained on a publicly available plant leaf dataset containing multiple classes such as:
Healthy
Bacterial Spot
Early Blight
Late Blight
Leaf Mold
Powdery Mildew
And more...
(You can mention the exact dataset name here if used.)
⚙️ Installation
Clone the repository:
Bash
Copy code
git clone https://github.com/your-username/plant-diseases-detection.git
cd plant-diseases-detection
Install dependencies:
Bash
Copy code
pip install -r requirements.txt
Or manually:
Bash
Copy code
pip install numpy pandas matplotlib seaborn tensorflow scikit-learn opencv-python
🏋️ Model Training
The CNN model is trained using:
Categorical Crossentropy Loss
Adam Optimizer
Accuracy as evaluation metric
Example training snippet:
Python
Copy code
model.compile(optimizer='adam',
              loss='categorical_crossentropy',
              metrics=['accuracy'])

history = model.fit(train_data,
                    validation_data=val_data,
                    epochs=30)
📈 Model Evaluation
Training Accuracy
Validation Accuracy
Loss Curve
Confusion Matrix
Classification Report
(Add your final accuracy here if available)
🔍 Prediction on New Image
Python
Copy code
from tensorflow.keras.models import load_model
from tensorflow.keras.preprocessing import image
import numpy as np

model = load_model("plant_disease_model.h5")

img = image.load_img("test_leaf.jpg", target_size=(224,224))
img_array = image.img_to_array(img) / 255.0
img_array = np.expand_dims(img_array, axis=0)

prediction = model.predict(img_array)
print("Predicted Class:", prediction)
🌱 Future Improvements
🔹 Deploy as Web App (Flask / Streamlit)
🔹 Mobile App Integration
🔹 Real-time camera detection
🔹 Transfer Learning (ResNet, MobileNet)
🔹 Model optimization for edge devices

 Detection using Deep Learning
- CNN + GradCAM Explainability
- Multi-GPU Training
- TensorFlow + Keras

🔗 Kaggle Notebook:
https://www.kaggle.com/code/ganeshratnala/plant-diseases-detection
