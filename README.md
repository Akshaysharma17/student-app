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
git clone <repository-url>
cd student-app
```

2. Install required packages:
```bash
pip install streamlit pandas numpy scikit-learn
```

### Running the Application
1. Start the Streamlit server:
```bash
streamlit run stud-per.py
```

2. Open your web browser and navigate to the local URL provided in the terminal (typically http://localhost:8501)

## Sample Data
Here are some example inputs and their expected predictions:

| Hours Studied | Previous Score | Extracurricular | Sleep Hours | Papers Solved | Expected Performance |
|--------------|----------------|-----------------|-------------|---------------|----------------------|
| 5            | 75            | Yes            | 7           | 5             | Good                 |
| 3            | 65            | No             | 6           | 3             | Average              |
| 8            | 85            | Yes            | 8           | 8             | Excellent            |

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

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Streamlit for the web interface framework
- Scikit-learn for machine learning capabilities
- Pandas and NumPy for data processing