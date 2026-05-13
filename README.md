Crop Recommendation System 🌿
This is a Flask-based web application that recommends the most suitable crop to cultivate based on soil and environmental parameters. By leveraging Machine Learning, the system analyzes inputs like Nitrogen, Phosphorus, Potassium levels, and weather conditions to provide accurate agricultural insights.

🚀 Features
Real-time Prediction: Get instant crop suggestions based on user input.

User-Friendly Interface: Simple web form for entering soil and climate data.

ML Pipeline: Utilizes pre-trained models and scalers (MinMaxScaler and StandardScaler) for high-quality predictions.

Extensive Database: Supports 22 different crops, including Rice, Maize, Coffee, and various fruits/pulses.

🛠️ Tech Stack
Backend: Flask (Python)

Data Processing: NumPy, Pandas

Machine Learning: Scikit-learn

Serialization: Pickle (for loading models/scalers)

Frontend: HTML/CSS (via Jinja2 templates)

📋 Prerequisites
Before running the project, ensure you have Python installed and the following libraries:

Bash
pip install flask numpy pandas scikit-learn
📂 Project Structure
Plaintext
├── app.py              # Main Flask application
├── model-2.pkl         # Trained ML model
├── standscaler.pkl     # Standard scaler object
├── minmaxscaler.pkl    # MinMax scaler object
├── templates/
│   └── index.html      # Web interface
└── README.md           # Project documentation
⚙️ How It Works
Input: The user enters values for Nitrogen (N), Phosphorus (P), Potassium (K), Temperature, Humidity, pH, and Rainfall.

Scaling: The raw data is first transformed using MinMaxScaler and then further processed by StandardScaler to match the training environment.

Prediction: The processed features are fed into the loaded .pkl model.

Output: The model returns a numeric label, which is mapped to a crop name using a dictionary and displayed on the web page.

🏃 How to Run
Clone this repository or save the files locally.

Ensure your model files (model-2.pkl, standscaler.pkl, minmaxscaler.pkl) are in the root directory.

Run the application:

Bash
python app.py
Open your browser and navigate to [http://127.0.0.1:5000/](http://127.0.0.1:5000/).
