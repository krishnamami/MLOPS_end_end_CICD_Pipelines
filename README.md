# 🚀  End to End MLOPS pipleines Implementation with CI/CD  using Jenkins on Google Cloud Platform (GCP)

This project demonstrates a complete MLOps workflow—from raw data ingestion to model deployment—leveraging CI/CD pipelines powered by Jenkins and hosted on Google Cloud Platform (GCP). It showcases best practices in building scalable, automated, and reproducible ML systems.


## 🎯 Project Objectives
- Automate ML pipeline from data ingestion to model deployment
- Use Jenkins to orchestrate CI/CD workflows
- Containerize and deploy ML models using Docker and Google Cloud Run
- Learn key concepts of MLOps, experiment tracking, and continuous training
  
## 🧠 Use Case: Hotel Booking Optimization
The model solves key problems in the hotel industry:
- **Revenue Management**: Handle overbookings and predict cancellations
- **Targeted Marketing**: Personalized ad targeting based on user behavior
- **Fraud Detection**: Identify suspicious booking patterns


![🚀 End-to-End MLOps Pipeline using Jenkins on GCP - visual selection](https://github.com/user-attachments/assets/455bf216-e7d5-4c81-8f62-6273936cabb8)


## 🔧 Tools and Technologies Used

|Category| Tools/Tech Used |
|--------|-------------|
| Data Storage	| Google Cloud Storage (GCS) |
| Model Training | Python, LightGBM, Scikit-learn |
| Tracking | MLflow |
| CI/CD | 	Jenkins, Git, Docker |
| Deployment | Google Cloud Run, Container Registry|
| App Layer | Flask (for prediction API) |

🔧 CI/CD Pipeline (Jenkins)
- Jenkins installed inside Docker container
- Pulls project repo from GitHub
- Sets up virtual environment & dependencies
- Builds and pushes Docker image to Google Container Registry (GCR)
- Deploys container to Google Cloud Run using service account credentials

✅ Key Features
- Modular Codebase for reusability and testing
- Fully Automated Deployment through Jenkins pipeline
- Experiment Tracking with MLflow for better model governance
- Flask App for serving predictions
  
📁 Project Structure
├── artifacts/                    # Stores all generated artifacts (raw data, processed data, models, etc.)
│
├── config/                       # Centralized config (e.g., model hyperparameters, GCP paths, thresholds)
│   └── config.yaml               # (Optional) Use YAML for easier editing outside code
│
├── custom_jenkins/              # Jenkins Docker setup for CI/CD pipeline
│   └── Dockerfile      # Add Jenkins to Docker
│
├── static/                    # CSS script to enhance UI
│   └── style.css
│ 
│
├── pipeline/                    # High-level orchestration scripts (e.g., triggering training)
│   └── training_pipeline.py     # Calls each pipeline step: ingestion → validation → training
│
├── src/                         # Core reusable modules (e.g., data_ingestion/, transformation/, utils/)
│   ├── data_ingestion.py
│   ├── data_preprocessing.py
│   ├── custome_exception.py
│   ├── model_training.py
│   └── logger.py
│
├── Dockerfile                   # Defines container image for training/deployment
│
├── Jenkinsfile                  # CI/CD pipeline steps (test → build → deploy)
│
├── application.py               # FastAPI / Flask app for prediction or monitoring endpoint
│
├── requirements.txt             # Python dependencies (pinned versions recommended)
│
└── setup.py   

## Acknowledgments
This project was created as part of my journey to deepen hands-on experience with MLOps, CI/CD practices, and cloud deployment strategies.

## Related Projects

[Distributed ML SageMaker Pipeline](https://github.com/krishnamami/Distributed_ML_Sagemaker_Pipelines)

Krishna Goud
Head of Data Engineering & MLOps | Rocket LA [LinkedIn](https://www.linkedin.com/in/krishnagoud)
