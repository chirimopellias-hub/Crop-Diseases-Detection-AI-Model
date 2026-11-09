# Crop Disease Detection AI Model

## 1. Project Overview

The **Crop Disease Detection AI Model** is an artificial intelligence and machine learning project developed to identify potential crop diseases from images of plant leaves.

The system uses **TensorFlow** to develop and run the machine learning model, with a dataset sourced from **Kaggle** for model development and evaluation. A **FastAPI** backend provides an API interface through which applications can submit crop images and receive prediction results.

The project explores how computer vision and artificial intelligence can support early crop disease identification, improve access to agricultural information, and contribute to more informed crop management decisions.

## 2. Project Objectives

The primary objectives are to:

- Develop an AI model capable of identifying crop diseases from plant images.
- Apply TensorFlow and machine learning techniques to image-based disease classification.
- Use an agricultural image dataset sourced from Kaggle for model development.
- Evaluate the model's performance using appropriate machine learning evaluation methods.
- Develop a FastAPI backend to expose the trained model through REST API endpoints.
- Provide a foundation for integrating AI-powered crop disease detection into web and mobile agricultural applications.

## 3. Key Features

### AI-Based Crop Disease Detection
Uses a trained TensorFlow model to analyse submitted plant images and generate disease classification predictions.

### Image-Based Classification
Processes crop images as model input to identify the corresponding trained classification category.

### FastAPI Integration
Provides a REST API interface for communication between the machine learning model and external applications.

### Prediction Service
Makes model predictions available through API requests and returns structured responses.

### Machine Learning Workflow
Supports the development lifecycle of an AI model, including dataset preparation, training, validation, evaluation, and inference.

## 4. Technology Stack

| Technology | Purpose |
|---|---|
| Python | Primary programming language |
| TensorFlow | Machine learning and deep learning model development |
| FastAPI | Backend API and model-serving framework |
| Kaggle | Source of the agricultural image dataset |
| Uvicorn | ASGI server for running the FastAPI application |


## 5. System Architecture

The project follows an AI inference architecture in which an external application communicates with a backend API that loads and executes the trained machine learning model.

```text
       Kaggle Dataset
              |
              v
      Dataset Preparation
              |
              v
      Image Preprocessing
              |
              v
     TensorFlow Model
              |
              v
       Model Training
              |
              v
       Model Evaluation
              |
              v
       Trained Model
              |
              v
       FastAPI Backend
              |
              v
       REST API Endpoint
              |
              v
      Image Submission
              |
              v
       Model Prediction
              |
              v
      Structured Response
```

### Architecture Components

**1. Dataset Layer**

The project uses an agricultural image dataset obtained from Kaggle as the source of image data for model development.

**2. Data Processing Layer**

Prepares image data for model consumption. Depending on the implementation, this may include resizing, normalization, labelling, and dataset splitting.

**3. Machine Learning Layer**

TensorFlow is used to develop and train the crop disease detection model.

**4. Model Serving Layer**

FastAPI exposes the trained model through HTTP endpoints, allowing external applications to submit images and request predictions.

**5. Client Integration Layer**

A web or mobile application can consume the API and display the prediction results.

## 5. Dataset

The model uses an image dataset sourced from Kaggle.

The dataset provides the image samples used during model development and evaluation.


## 6. Machine Learning Development

TensorFlow is used for the development and execution of the crop disease detection model.

The machine learning workflow includes:

1. Dataset collection.
2. Image preprocessing.
3. Model development.
4. Model training.
5. Model validation.
6. Performance evaluation.
7. Model saving and loading.
8. Prediction using new images.


## 7. FastAPI Backend

FastAPI provides the backend interface for accessing the trained TensorFlow model.

The API is responsible for:

- Accepting image upload requests.
- Validating incoming image files.
- Preparing images for model inference.
- Loading and executing the trained model.
- Returning structured prediction responses.
- Providing API documentation through its interactive documentation interface.

### API Documentation

When the FastAPI application is running locally, its interactive documentation is generally available at:

- Swagger UI: `http://127.0.0.1:8000/docs`
- ReDoc: `http://127.0.0.1:8000/redoc`

The exact API endpoints depend on the implemented routes.

## 8. Installation and Setup

### Prerequisites

Install the following:

- Python (compatible with the project's TensorFlow version)
- pip
- Git

### Step 1: Clone the Repository

```bash
git clone https://github.com/chirimopellias-hub/Crop-Diseases-Detection-AI-Model.git
```

Navigate into the project directory:

```bash
cd chirimopellias-hub
```

### Step 2: Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

On Linux or macOS:

```bash
source venv/bin/activate
```

### Step 3: Install Dependencies

If the repository contains a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

Otherwise, install the dependencies specified by your implementation.

### Step 4: Configure the Model

Ensure the trained TensorFlow model is available at the location expected by the FastAPI application.

If the model is not included in the repository, follow the project's model download or training instructions.

### Step 5: Start the FastAPI Server

For an application whose entry point is `app/main.py` and whose FastAPI instance is named `app`:

```bash
uvicorn app.main:app --reload
```

Adjust the command to match the actual project structure.

### Step 6: Access the API

Open:

```text
http://127.0.0.1:8000/docs
```

Use the interactive API documentation to inspect and test the implemented endpoints.

## 9. Example API Workflow

The general prediction workflow is:

1. A client submits a crop image to the API.
2. FastAPI receives and validates the image.
3. The backend preprocesses the image.
4. The TensorFlow model performs inference.
5. The API returns the prediction response.

An illustrative response structure could look like this:

```json
{
  "prediction": "Predicted class",
  "confidence": 0.95
}
```

## 11. Potential Applications

The project provides a foundation for applications such as:

- Agricultural disease identification platforms.
- AI-powered farming advisory systems.
- Digital agriculture applications.
- Crop monitoring and decision-support solutions.
- Web and mobile agricultural technology platforms.

These are potential applications and do not necessarily represent completed integrations.

## 12. Future Improvements

Possible future development areas include:

- Expanding the dataset to cover additional crops and disease categories.
- Improving model generalisation using more diverse images.
- Evaluating model performance across different environmental conditions.
- Integrating the API with a React-based web application.
- Developing a mobile application for field-based image submission.
- Deploying the API using a suitable cloud infrastructure.
- Implementing automated model testing and deployment through CI/CD.
- Adding confidence thresholds and clear uncertainty handling.
- Providing agricultural guidance based on verified disease information.

## 13. Responsible Use and Limitations

Model predictions should be treated as decision-support information rather than a definitive agricultural diagnosis.

Prediction reliability depends on the quality, diversity, labelling, and representativeness of the training dataset. Image conditions that differ significantly from the training data may affect performance.

Where necessary, farmers should seek confirmation from qualified agricultural professionals before making important crop-management decisions.

## 14. Skills Demonstrated

This project demonstrates practical experience and learning in:

- Python programming.
- Artificial intelligence and machine learning.
- TensorFlow model development.
- Image classification.
- Image preprocessing.
- Dataset preparation and management.
- Model training and evaluation.
- REST API development.
- FastAPI backend development.
- Machine learning model integration.

## 15. Author

**Developed by:** Pellias Chirimo

**Project:** Crop Disease Detection AI Model
