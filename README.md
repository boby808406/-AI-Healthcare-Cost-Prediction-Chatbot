AI-Healthcare-Cost-Prediction-Chatbot

An AI-powered healthcare chatbot built with Flask and Machine Learning that predicts estimated hospital costs based on a patient's Age, Gender, and Medical Condition. The chatbot uses a trained Random Forest Regression model to provide instant cost estimates through a clean conversational interface.

Demo
Example interaction:

User: predict cost
Bot: Please provide details in this format: Age, Gender (Male/Female), Condition
User: 20, male, fever
Bot: 💰 The estimated hospital cost is approximately ₹100.00


🚀 Features

💬 Conversational chatbot interface (web-based)
💰 Predicts hospital cost based on Age, Gender, Condition
🤖 ML model: Random Forest Regressor (~trained on real hospital data)
🔄 Multi-turn conversation with session state management
⚠️ Input validation with helpful error messages
🌐 Built with Flask — runs locally in any browser


🛠️ Tech Stack
LayerTechnologyFrontendHTML, CSS, JavaScriptBackendPython, FlaskML ModelScikit-learn (Random Forest Regressor)Data ProcessingPandas, NumPyModel PersistenceJoblibPreprocessingStandardScaler, One-Hot Encoding

📂 Project Structure
ai-healthcare-chatbot/
├── app.py                        # Flask web application
├── chatbot.py                    # Chatbot logic & ML prediction
├── train_model.py                # Model training script
├── demo.png                      # App screenshot
├── requirements.txt              # Python dependencies
├── hospital data analysis.csv    # Training dataset
├── model/
│   ├── cost_model.pkl            # Trained Random Forest model
│   └── scaler.pkl                # Fitted StandardScaler
└── templates/
    └── index.html                # Chat UI

⚙️ How to Run Locally
1. Clone the repository
bashgit clone https://github.com/boby808406/ai-healthcare-chatbot.git
cd ai-healthcare-chatbot
2. Install dependencies
bashpip install -r requirements.txt
3. Train the model (first time only)
bashpython train_model.py
4. Run the Flask app
bashpython app.py
5. Open your browser
http://localhost:5000

📦 Requirements
Create a requirements.txt with:
flask
scikit-learn
pandas
numpy
joblib

🤖 How the ML Model Works

Dataset: Hospital records with Age, Gender, Medical Condition, and Cost columns
Preprocessing:

Gender encoded: Male = 0, Female = 1
Condition encoded using One-Hot Encoding
Features scaled using StandardScaler


Model: Random Forest Regressor (100 estimators)
Prediction: Given new patient details → model predicts estimated hospital cost


💡 Key Insights

Young patients (Age 15–25) with common conditions (Fever, Cold) have lower predicted costs (~₹100–₹500)
Chronic conditions result in significantly higher cost predictions
Gender and age both influence cost prediction through learned patterns in training data


🎯 Future Improvements

 Add readmission risk prediction feature
 Connect to real hospital dataset for better accuracy
 Add insurance coverage estimator
 Deploy on cloud (Render / Heroku)
 Add voice input support


👤 Author
Rachuri Boby Nikhil
Data Analyst | Python • Flask • Machine Learning
📧 rachuribobynikhil.123@gmail.com
🔗 LinkedIn https://www.linkedin.com/in/boby-nikhil-8181302ba | GitHub  https://github.com/boby808406/boby808406
