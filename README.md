# Bangalore House Price Prediction

A machine learning web application that predicts house prices in Bangalore based on location, total square footage, number of bathrooms, and BHK configuration. The application uses a trained Ridge Regression model and a Flask web interface to provide price estimates.

## Features

- Predicts estimated house prices in Bangalore.
- Uses location, square footage, bathrooms, and BHK as inputs.
- Applies a trained machine learning pipeline for prediction.
- Provides a web interface built with HTML, CSS, and JavaScript.
- Uses Flask to connect the frontend with the machine learning model.

## Technologies Used

- **Python** — application logic
- **Pandas & NumPy** — data processing
- **Scikit-learn** — machine learning and preprocessing
- **Ridge Regression** — prediction model
- **Flask** — web application backend
- **HTML, CSS & JavaScript** — frontend

## Project Structure

```text
bangalore-house-price-prediction/
├── app.py
├── Cleaned_data.csv
├── RidgeModel.pkl
├── requirements.txt
├── README.md
├── templates/
│   └── index.html
└── static/
    ├── style.css
    └── script.js
```

The `static/` directory is optional if your CSS and JavaScript are included directly in `index.html`.

## Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd bangalore-house-price-prediction
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### 2. Create a virtual environment (optional)

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
python app.py
```

Open the following URL in your browser:

```text
http://127.0.0.1:5001
```

## How It Works

1. The user enters the location, square footage, number of bathrooms, and BHK configuration.
2. Flask collects the input and converts it into a Pandas DataFrame.
3. The trained Ridge Regression pipeline processes the inputs and predicts the price.
4. The application converts the model output into an estimated price in rupees and displays the result.

## Model

The project uses a trained Ridge Regression model saved in `RidgeModel.pkl`. The model expects the input features in the following order:

- `location`
- `total_sqft`
- `bath`
- `bhk`

The prediction output is multiplied by `100000` to convert it into the displayed price in rupees, based on the training target's scale.

## Future Improvements

- Add model evaluation metrics such as MAE, RMSE, and R².
- Improve input validation and error handling.
- Deploy the application online.
- Enhance the user interface and mobile responsiveness.

## Disclaimer

Predicted prices are estimates based on the training data and model. They should not be treated as official property valuations or
