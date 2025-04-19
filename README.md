# Student Performance Prediction System

## Overview
This project is a web-based application that predicts student performance using machine learning. It provides an interactive interface where users can input various parameters related to their study habits and receive a performance prediction.

## Features
- Interactive web interface built with Streamlit
- Machine learning model for performance prediction
- Real-time predictions based on user input
- User-friendly input fields with validation
- Standardized data preprocessing pipeline

## Technical Stack
- **Frontend**: Streamlit
- **Backend**: Python
- **Machine Learning**: Scikit-learn
- **Data Processing**: Pandas, NumPy
- **Model Persistence**: Pickle

## Input Parameters
The system takes the following parameters to make predictions:
1. Hours Studied (1-10 hours)
2. Previous Scores (40-100)
3. Extracurricular Activities (Yes/No)
4. Sleep Hours (4-10 hours)
5. Number of Question Papers Solved (0-10)

## Getting Started

### Prerequisites
- Python 3.7+
- pip (Python package installer)

### Installation
1. Clone the repository:
```bash
git clone https://github.com/Akshaysharma17/student-app.git
cd student-app
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

### Running the Application
1. Start the Streamlit server:
```bash
streamlit run stud-per.py
```

2. Open your web browser and navigate to the local URL provided in the terminal (typically http://localhost:8501)

## Sample Data
Here are some real examples from the training dataset:

| Hours Studied | Previous Score | Extracurricular | Sleep Hours | Papers Solved | Performance Index |
|--------------|----------------|-----------------|-------------|---------------|-------------------|
| 7            | 99            | Yes            | 9           | 1             | 91.0              |
| 4            | 82            | No             | 4           | 2             | 65.0              |
| 8            | 51            | Yes            | 7           | 2             | 45.0              |
| 5            | 52            | Yes            | 5           | 2             | 36.0              |
| 7            | 75            | No             | 8           | 5             | 66.0              |
| 3            | 78            | No             | 9           | 6             | 61.0              |

### Performance Index Interpretation
- 90-100: Excellent
- 80-89: Very Good
- 70-79: Good
- 60-69: Above Average
- 50-59: Average
- 40-49: Below Average
- 30-39: Poor
- 20-29: Very Poor

## Model Details
- The system uses a trained machine learning model stored in `student_lr_final_model.pkl`
- The model includes:
  - A trained classifier
  - A StandardScaler for feature normalization
  - A LabelEncoder for categorical variables

## Data Preprocessing
The system automatically:
1. Encodes categorical variables (Extracurricular Activities)
2. Normalizes numerical features using StandardScaler
3. Prepares the data in the correct format for prediction

## Usage
1. Fill in all the required fields in the web interface
2. Click the "predict-your_score" button
3. View your predicted performance score

## Contributing
Feel free to submit issues and enhancement requests!

## Acknowledgments
- Streamlit for the web interface framework
- Scikit-learn for machine learning capabilities
- Pandas and NumPy for data processing
