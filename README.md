
# Breast Cancer Analysis and Prediction Model API

This repository contains a FastAPI application that serves a machine learning model for predicting breast cancer. Users can submit patient data in JSON format to get predictions on the likelihood of breast cancer.

## Application Overview

- **Input**: Accepts patient data in JSON format.
- **Output**: Returns predictions in JSON format, including the probability of breast cancer.
- **Fast and Scalable**: Built on FastAPI, providing quick and scalable API responses.

### How It Works:
1. **Submit Data**: Send relevant patient features (e.g., mean radius, texture, etc.) via a POST request.
2. **Get Prediction**: The model processes the data and predicts the likelihood of breast cancer.
3. **Response**: A JSON response is returned with the prediction and its probability.

### Example Input:
\`\`\`json
{
    "feature_values": {
        "radius_mean": 14.3,
        "texture_mean": 20.1,
        "perimeter_mean": 132.4,
        "area_mean": 1010.3,
        "smoothness_mean": 0.1184
    }
}
\`\`\`

### Example Output:
\`\`\`json
{
  "predicted_cancer_type": "Malignant"
}
\`\`\`
