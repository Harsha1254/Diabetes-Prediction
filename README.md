# Diabetes Prediction Project

# Overview

This project leverages machine learning to predict diabetes status, focusing on early detection to enhance healthcare outcomes. It utilizes the "Diabetes Prediction Dataset by iammustafatz," a diverse dataset encompassing 100,000 records of men and women. The model analyzes key health metrics such as age, body mass index (BMI), HbA1c level, and blood glucose level to classify patients as diabetic or non-diabetic. The primary goal is to provide a robust, generalizable predictive tool for clinicians, supporting timely interventions. The project employs advanced techniques like data preprocessing, model training with algorithms such as K-Nearest Neighbors (KNN) and Decision Trees, and performance evaluation, achieving high accuracy. Detailed documentation accompanies the codebase, offering insights into methodologies, results, and potential improvements.

Setup

To run this project locally, follow these steps:





Clone the Repository:
Use the command git clone <repository-url> to download the project to your local machine. Replace <repository-url> with the actual URL of your GitHub repository.



Install Dependencies:
Navigate to the project directory and install required Python libraries by running:
pip install -r requirements.txt
Ensure a requirements.txt file is included, listing dependencies such as pandas, numpy, scikit-learn, seaborn, and matplotlib. Example content for requirements.txt:

pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
seaborn>=0.11.0
matplotlib>=3.4.0



Set Up Environment:
It’s recommended to use a virtual environment:





Create: python -m venv venv



Activate: source venv/bin/activate (Linux/Mac) or venv\Scripts\activate (Windows)



Install dependencies as above.



Run the Project:
Execute the main script or notebook: python main.py or open diabetes_prediction.ipynb in Jupyter Notebook. Adjust the file name based on your project structure.

Usage





Training and Testing: Run the script or notebook to train the KNN and Decision Tree models on the preprocessed dataset. The code automatically splits data into training and testing sets, scales features, and evaluates model performance.



Prediction Function: Use the implemented predict_diabetes function to classify new patient data. Input a dictionary with patient metrics (e.g., age, BMI, HbA1c) and receive a "Diabetic" or "Non-Diabetic" output.



Output Review: Check generated output files (e.g., accuracy scores, confusion matrices) or visualizations (e.g., correlation heatmaps) saved in the project directory. Results are also logged in the notebook or console.



Customization: Modify hyperparameters (e.g., KNN’s n_neighbors, Decision Tree’s max_depth) in the code to experiment with model performance.

Results





Model Performance: Achieved accuracies of approximately 96.0% for KNN and 97.2% for Decision Tree, though these were influenced by dataset imbalance (91.5% non-diabetic). Post-SMOTE, test accuracies stabilized around 92-93% with improved recall for diabetic cases.



Key Predictors: Analysis identified HbA1c level and blood glucose level as the most significant predictors of diabetes, validated through correlation analysis and model feature importance.



Limitations: The dataset’s "No Info" category in smoking history introduces noise, and imbalance affects minority class prediction. Future iterations should address these.



Practical Utility: The prediction function successfully classified sample patients, e.g., a 60-year-old male with HbA1c 7.5 as "Diabetic."

Future Work





Algorithm Enhancement: Integrate advanced models like Random Forest or XGBoost to improve accuracy and handle imbalance.



Deployment: Develop a web application using Flask or Streamlit for real-time predictions in clinical settings.



Data Expansion: Incorporate additional datasets or impute "No Info" values to reduce noise and enhance model robustness.



Evaluation Metrics: Expand analysis with precision, recall, and F1-score to better assess performance on diabetic cases.

Contributing

We welcome contributions to improve this project! Follow these steps:





Fork the repository to your GitHub account.



Create a new branch: git checkout -b feature-branch.



Make changes and commit: git commit -m "Describe your changes".



Push to your fork: git push origin feature-branch.



Submit a pull request with a clear description of your updates.





Ensure code adheres to PEP 8 style guidelines.



Add unit tests if introducing new features, and update documentation accordingly.

License

This project is licensed under the MIT License. See the LICENSE file for details. Feel free to use, modify, and distribute the code, provided you include the original copyright notice.
