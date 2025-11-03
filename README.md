# California Housing Price Prediction

This project implements a machine learning model to predict housing prices in California based on various features such as median income, house age, average rooms, etc.

## Project Overview
- Implements a Linear Regression model for price prediction
- Uses the California Housing dataset from scikit-learn
- Provides both API and web interface for predictions
- Features data preprocessing and model serialization

## Features
- Data preprocessing using StandardScaler
- Model training using Linear Regression
- Flask web application for user interface
- REST API endpoint for programmatic access
- Interactive web form for input submission

## Directory Structure
```
califoniahouseprising_ML/
├── AI_HousePrediction (1).ipynb   # Main notebook with model development
├── app.py                         # Flask application
├── templates/                     # HTML templates
│   └── home.html                 # Main prediction interface
├── regmodel.pkl                  # Serialized regression model
├── scaler.pkl                    # Serialized data scaler
└── requirement.txt               # Project dependencies
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/BhargavDevi/califoniahouseprising_ML.git
cd califoniahouseprising_ML
```

2. Create a new conda environment:
```bash
conda create -p venv python=3.8 -y
conda activate venv/
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Deployment on Render

1. Create a new Web Service on Render
2. Connect your GitHub repository
3. Use the following settings:
   - Environment: Python
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `python app.py`
4. Add the following environment variables if needed:
   - `PYTHON_VERSION`: 3.8 (or your preferred version)

## Required Packages
- Flask
- scikit-learn
- pandas
- numpy
- matplotlib
- seaborn (for visualization)

## Usage

1. Start the Flask application:
```bash
python app.py
```

2. Access the web interface:
- Open your browser and navigate to `http://localhost:5000`
- Enter the required housing features in the form
- Click submit to get the price prediction

3. API Usage:
```bash
POST /predict_api
Content-Type: application/json

{
    "data": {
        "MedInc": value,
        "HouseAge": value,
        "AveRooms": value,
        "AveBedrms": value,
        "Population": value,
        "AveOccup": value,
        "Latitude": value,
        "Longitude": value
    }
}
```

## Model Information
- Algorithm: Linear Regression
- Features: 8 input features (median income, house age, average rooms, etc.)
- Preprocessing: Standard scaling of input features
- Output: House price prediction in $10000s units

## Development
- The model is developed in the Jupyter notebook `AI_HousePrediction (1).ipynb`
- Data preprocessing and model training steps are documented in the notebook
- The Flask application (`app.py`) serves both web interface and API endpoints

## Tools Used
1. [GitHub](https://github.com) - Version Control
2. [VS Code](https://code.visualstudio.com/) - IDE
3. [Python 3.8](https://www.python.org/) - Programming Language
4. [Flask](https://flask.palletsprojects.com/) - Web Framework
5. [scikit-learn](https://scikit-learn.org/) - Machine Learning Library

## License
This project is licensed under the included License file.

## Author
Bhargav Devi Prasad S