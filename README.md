# LeafLifePredictor: Deforestation Prediction Model

This project develops a neural network-based model to predict deforestation using historical satellite and geographical data. The model aims to identify areas at risk of deforestation, aiding in more effective resource allocation and conservation efforts.

![Forest Forecast Model](/Imagess/forest.jpg)

## Overview

A  Sequential neural network engineered to predict areas at risk of deforestation and offer crucial notifications to underserved regions with limited internet and power access. This innovative solution utilizes LoRa communication technology to send timely alerts, enhancing environmental protection efforts. Additionally, the predictions of potential deforestation areas can be viewed on a website featuring a 3D map, providing an interactive and detailed visualization of regions vulnerable to tree loss. This tool is a vital asset in combating deforestation and aiding conservation efforts in remote areas.

## About Us
In response to the global trend of deforestation driven by factors such as agriculture, logging, and urban expansion, the region of Jalisco, Mexico, has emerged as one of the areas within Mexico grappling with significant deforestation challenges. To address this critical situation, we are developing a computer program designed to predict areas at risk of deforestation effectively.

Furthermore, our project includes the creation of a website featuring a 3D map that displays areas at high risk of deforestation. This map also indicates where alerts have been dispatched, providing crucial information for conservation efforts. This resource serves as a valuable decision-making tool for various stakeholders, including environmental agencies, local authorities, and the general public seeking up-to-date information.

Our objective is to employ advanced computer tools and specialized alert systems to notify individuals and organizations when an area is at an imminent risk of deforestation, particularly in remote and difficult-to-access areas. This effort is vital for mobilizing rapid response and conservation strategies to prevent further environmental degradation.

## Model Workflow

1. **Data Preprocessing**
   - **Normalization**: Features are scaled between 0 and 1 to facilitate faster and more stable training.
   - **Handling Missing Values**: Rows with missing data are dropped to maintain data integrity.
   - **Feature Scaling**: Features are standardized to minimize bias toward features with larger scales.

2. **Class Imbalance Handling**
   - **SMOTE (Synthetic Minority Over-sampling Technique)**: Balances the dataset by synthetically oversampling the minority class.

3. **Model Building and Tuning**
   - **Sequential Model**: Utilizes layers of neurons with activation functions, batch normalization, and dropout layers to manage overfitting.
   - **Hyperparameter Tuning**: Employs Keras Tuner's Hyperband, optimizing model parameters efficiently.
   - **Early Stopping**: Monitors validation loss to stop training when the model performance no longer improves, preventing overfitting.

4. **Model Evaluation**
   - **Metrics**: Uses accuracy, confusion matrix, and classification reports to evaluate performance.
   - **False Positives/Negatives Analysis**: Important for understanding the model's impact on resource allocation and conservation efforts.

5. **Visualization**
   - **Training and Validation Metrics**: Plots of accuracy and loss over epochs to visualize learning and generalization.

## Technologies Used

- **Pandas & NumPy**: For data manipulation and numerical operations.
- **Scikit-learn**: Provides tools for data splitting, feature scaling, and performance metrics.
- **Keras**: For building the neural network model.
- **Keras Tuner**: For optimizing the neural network architecture and parameters.
- **Matplotlib**: For plotting training and validation metrics.
- **Imbalanced-Learn (imblearn)**: For handling class imbalance using SMOTE.

## Requirements

Before running the model, ensure you have Python 3.x installed. To run this model, follow these steps to set up your environment:

1. **Install Python 3.x**
   - Download from [Python's official site](https://python.org).

2. **Create a Virtual Environment**
   - Open a terminal or command prompt.
   - Navigate to your project directory: `cd path_to_project`
   - Create a virtual environment: `python -m venv env`

3. **Activate the Virtual Environment**
   - **Windows**: `.\env\Scripts\activate`
   - **MacOS/Linux**: `source env/bin/activate`

4. **Install Required Libraries**
   ```bash
   pip install pandas numpy scikit-learn keras keras-tuner matplotlib imbalanced-learn
## Important Considerations
- Data Quality: The accuracy of predictions heavily depends on the quality and relevance of the input data.
- Model Bias: Adjustments in the model evaluation metrics or loss functions might be necessary to align the model better with specific conservation goals.
- Computational Resources: Hyperparameter tuning and training deep learning models can be resource-intensive. Adequate computational resources are recommended.
