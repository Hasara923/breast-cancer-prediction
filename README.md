
# Breast Cancer Analysis and Prediction Model API

This repository contains a FastAPI application that serves a machine learning model for predicting breast cancer. The application exposes an API endpoint where users can submit patient data in JSON format and receive predictions regarding the likelihood of breast cancer.

## Application Overview

This FastAPI app offers an efficient interface for interacting with a trained machine learning model, designed to assist in early diagnosis and support decision-making processes in clinical settings.

### Key Features:
- **JSON-based Input**: The API accepts input in JSON format for easy integration with various applications.
- **Structured Output**: Predictions are returned in JSON format, including the probability of cancer and relevant insights.
- **Scalable and Fast**: The application is built on FastAPI, providing a scalable and fast solution even for large datasets.
- **Automated CI/CD**: Implements CI/CD pipeline using GitHub Actions to automatically build, test, and deploy the application with every code update.

### How It Works:
1. **Submit Patient Data**: The API accepts input features (e.g., mean radius, texture, perimeter) in JSON format.
2. **Prediction Generation**: The input data is processed by the machine learning model, which predicts the likelihood of breast cancer.
3. **Receive Response**: A JSON response is returned with the prediction and associated metadata.

### Example Input:
```bash
{
    "feature_values": {
        "radius_mean": 14.3,
        "texture_mean": 20.1,
        "perimeter_mean": 132.4,
        "area_mean": 1010.3,
        "smoothness_mean": 0.1184
    }
}
```
![1](https://github.com/user-attachments/assets/818a9951-43c0-4f8f-b40d-e2c0349564da)


### Example Output:
```json
{
  "predicted_cancer_type": "Malignant"
}
```
![2](https://github.com/user-attachments/assets/6e4917cf-00a9-483c-b289-ca7020dff760)

## Deployment Overview

The FastAPI application is deployed on **Azure App Service**, a fully managed platform that ensures seamless deployment and scalability of web applications. By leveraging Azure, the application benefits from features like automatic scaling, high availability, and integration with other Azure services, making it suitable for real-world usage.

### Deployment Steps:
1. **Create a Container App**: Use the Azure portal to create a container app for the FastAPI application.
2. **Configure Docker**: Set the Docker image and tag (from Docker Hub) for the app.
3. **Expose API**: Enable ingress and configure the app to listen on the correct port (e.g., 8000).
4. **Deploy**: After reviewing all settings, deploy the container app, which will take a few minutes.

---

## CI/CD Pipeline

This project includes a CI/CD pipeline to automate the build and deployment process using GitHub Actions and Docker.

### Pipeline Overview
- **Pipeline Name**: FastAPI Docker Build and Push
- **Purpose**: Automatically build and push a Docker image to Docker Hub upon pushing code to the main branch.
- **Tools**:
  - **GitHub Actions**: For CI/CD automation.
  - **Docker**: To containerize the application.
  - **Docker Hub**: To store and distribute the built image.

### Demo
You can make requests to the following URL:
```bash
https://cancer-prediction-08.proudpebble-12d2fb1c.australiaeast.azurecontainerapps.io/docs
```
