🚗 Car Brand Detector

This project is a deep learning–powered car brand classification system built with TensorFlow/Keras. It can classify images of cars into 7 categories and also supports real-time webcam detection.

📌 Features

Upload a car image through a Flask web app and get the predicted brand with confidence score.

Supported classes:

Audi

Hyundai Creta

Mahindra Scorpio

Rolls Royce

Swift

Tata Safari

Toyota Innova

Webcam live detection using OpenCV.

Displays real-time predictions with confidence overlay.

🛠️ Installation
1. Clone the repository
git clone https://github.com/yourusername/carmodel-detector.git
cd carmodel-detector

2. Create and activate virtual environment
python -m venv venv
venv\Scripts\activate   # On Windows
source venv/bin/activate # On Linux/Mac

3. Install dependencies
pip install -r requirements.txt


requirements.txt example:

Flask
tensorflow
numpy==1.23.5
opencv-python==4.7.0.72
matplotlib

🚀 Usage
1. Run Flask app (image upload detection)
python app.py


Then open in your browser:
👉 http://127.0.0.1:5000/

Upload an image, and the model will display the predicted brand and confidence score.

2. Run Webcam Live Detection
python webcam_detector.py


A window will open showing your webcam feed.

Predictions will appear on top of each frame.

Press q to quit.

📂 Project Structure
carmodel-detector/
│── app.py               # Flask app for image upload detection
│── webcam_detector.py   # OpenCV-based live webcam detection
│── carmodel.h5          # Trained Keras model
│── uploads/             # Folder to store uploaded images
│── templates/
│   └── index.html       # Web app frontend
│── requirements.txt     # Dependencies
│── README.md            # Project documentation

📊 Model Training

Trained on a custom dataset of 7 car brands.

Image size: 128x128.

Accuracy achieved: 96%+ on training set.

📸 Example

Web app upload result:
Audi (Confidence: 97.52%)

Webcam live detection:
Real-time overlay of car brand prediction on video frames.

✅ Future Improvements

Add support for more car brands.

Improve generalization with larger dataset.

Deploy model on cloud (AWS/GCP/Heroku).

Add top-3 predictions for better explainability.

👨‍💻 Author

Vaibhava Poojary
AI/ML & GenAI Engineer | AWS | TensorFlow | LangChain
