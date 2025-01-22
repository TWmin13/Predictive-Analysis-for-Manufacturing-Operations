# Predictive-Analysis-for-Manufacturing-Operations
created a RESTful API to predict machine downtime using a manufacturing dataset. 

**Predictive Maintenance API**

Setup Instructions

1. Install Dependencies

pip install fastapi uvicorn pandas numpy scikit-learn opendatasets

2. Download Dataset from Kaggle

Make sure you have a Kaggle API key.

Place the kaggle.json file in ~/.kaggle/ (Linux/Mac) or C:\Users\<YourName>\.kaggle\ (Windows).

The script will automatically download the dataset.

3. Run the API

python script.py

--------------------------------------------------------------------------------------------------------

**API Endpoints**

1. Train Model

Endpoint:

POST /train

Example cURL Request:

curl -X POST http://127.0.0.1:8000/train

Example Response:

{
  "message": "Model trained successfully",
  "accuracy": 0.85,
  "f1_score": 0.82
}

2. Make Prediction

Endpoint:

POST /predict

Example cURL Request:

curl -X POST http://127.0.0.1:8000/predict -H "Content-Type: application/json" -d '{"Temperature": 300, "Run_Time": 1200}'

Example Response:

{
  "Downtime": "Yes",
  "Confidence": 0.87
}

-------------------------------------------------------------------------------------------------------------------

**Testing with Postman**

Open Postman.

Use the POST method for /train and /predict.

Send JSON payloads to /predict.

--------------------------------------------------------------------------------------------------------------------

**Troubleshooting**

Ensure uvicorn is running properly.

Check dataset file paths.

Ensure the correct Python environment is active.


