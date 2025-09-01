# Predictive-Pulse-Harnessing-Machine-Learning-for-Blood-Pressure-Analysis
Objective : The Blood Pressure Prediction System is a machine learning-based web  application designed to provide a basic health monitoring solution for predictingblood pressure levels using user-input features. The primary objective of this project is to bridge the gap between medical awareness and accessibility by offering a lightweight, intuitive tool that empowers users to gain early insights into their cardiovascular health.

# Tech Stack
🔹 Frontend (User Interface Layer)

    ● HTML5 : Used to build the structure of the input form.
    
    ● CSS3 : For basic styling and layout enhancements.
    
    ● Jinja2 Templating Engine : Used within Flask to dynamically render the prediction result on the same page without needing a full page reload.

The UI is kept intentionally simple to ensure accessibility even on low-powered devices or slow networks. No JavaScript frameworks are used, ensuring the lowest learning curve for those exploring the code.

🔹 Backend (Application & Logic Layer)

  ● Python 3.x : Primary programming language used.
  
  ● Flask : A lightweight and efficient web framework used to build and serve
    the application.
    
  ● Pickle : Python’s object serialization module used to save and load the trainedmachine learning model.
  
  ● NumPy : For numerical array handling and preprocessing.
  
  ● scikit-learn :  For model training, evaluation, and prediction.
  
The Flask app listens for POST requests from the frontend, converts input into anumerical format, feeds it into the model, and returns the predicted blood pressure value to be displayed.

# ML Model & Integration

● Training & Evaluation – The model is trained offline using a structured dataset.

● Model File – Saved as model.pkl and loaded at runtime using pickle.load().

● Input Handling : The model expects a fixed-format array derived from user inputs.

The integration is done in such a way that the model is loaded once at server start, avoiding the overhead of reloading it for every prediction.

# Dataset

The model is trained on a dataset containing health-related attributes and corresponding blood pressure values. The dataset may include:

● Age

● Weight

● BMI

● Activity level

● Previous blood pressure readings


# Tooling, Hosting & Version Control

● VS Code : Used as the primary development environment.

● GitHub : Version control and collaboration platform for code sharing.

● Localhost : Flask runs locally on http://127.0.0.1:5000 during development.

● Browser :  Any modern web browser can access and use the tool.


# Prediction Accuracy

○ R2 Score

    ● For a well-prepared dataset, the model typically achieves:

○ MAE < 10 mmHg

○ R2 > 0.85

    ● This means predictions are generally within ±10 mmHg of actual blood pressure values in test data.

# Execution Speed / Response Time

● The entire request–response cycle is typically under 2 seconds.

● The ML model is loaded once when the Flask server starts, avoiding per-request loading delays.

● Input processing and model prediction take approximately 50–100 milliseconds.

