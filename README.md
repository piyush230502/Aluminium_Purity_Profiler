Aluminium rod quality refers to the characteristics and properties that determine the suitability of aluminium rods for various applications 
- Strength-to-weight ratio: Aluminium rods are strong yet lightweight, making them ideal for applications where weight is a concern.
- Corrosion resistance: Aluminium naturally resists corrosion, which makes it durable in harsh environments.
- Machinability: Aluminium rods are easy to machine, allowing for precise shaping and cutting.
- Thermal and electrical conductivity: Aluminium has excellent conductivity properties, making it useful in electrical and thermal applications.
- Formability: Aluminium rods can be easily formed into various shapes without losing their strength.


#### Dataset is taken from Kaggle and stored in mongodb


💿 Installing
1. Environment setup.
```
conda create --prefix venv python==3.8 -y
```
```
conda activate venv/
````
2. Install Requirements and setup
```
pip install -r requirements.txt
```
5. Run Application
```
python app.py
```

🔧 Built with
- flask
- Python 3.8
- Machine learning
- Scikit learn
- 🏦 Industrial Use Cases


### Problem Statement

The production of aluminum wire rods requires precise control over various dynamic parameters, such as chemical composition, casting temperature, and rolling mill conditions, to ensure optimal quality. Traditionally, the quality control in aluminum wire rod production has relied on manual methods, which can lead to inefficiencies in productivity and potential inconsistencies in product quality. The aim is to develop a predictive AI/ML model that can forecast the physical properties of aluminum wire rods based on these parameters, allowing for real-time adjustments to maintain high-quality standards.

### Aim

The primary aim is to build a predictive model using machine learning techniques to estimate key physical properties of aluminum wire rods, such as Ultimate Tensile Strength (UTS), elongation, conductivity, and overall rod quality. This model will enable manufacturers to optimize the wire rod production process by adjusting input parameters, thereby improving productivity and quality control.

### Objectives

1. **Data Understanding and Preprocessing**: 
   - Analyze the provided dataset to understand the relationship between input parameters (such as casting temperature, emulsion pressure, etc.) and output variables (UTS, elongation, conductivity, and rod quality).
   - Clean and preprocess the data to handle any missing values, outliers, or noise in the dataset.

2. **Feature Selection and Engineering**: 
   - Identify the most influential features from the dataset that have the highest correlation with rod quality.
   - Engineer new features if necessary to enhance the predictive power of the model.

3. **Model Development**: 
   - Build and evaluate machine learning models (such as linear regression, decision trees, random forests, or neural networks) to predict the output properties of the wire rods.
   - Compare the performance of different models based on evaluation metrics like accuracy, mean squared error (MSE), and F1 score.

4. **Model Validation and Tuning**: 
   - Perform hyperparameter tuning to improve the accuracy and generalization of the selected model.
   - Cross-validate the model to ensure that it works effectively across different subsets of the data.

5. **Integration for Real-time Feedback**: 
   - Explore the possibility of integrating the developed model into a real-time monitoring system for continuous quality control during production.
   - Provide insights on how the production team can adjust process parameters based on model predictions.

### Tools and Technologies Required

1. **Programming Languages**: 
   - Python: For data manipulation, analysis, and building machine learning models using libraries such as NumPy, pandas, scikit-learn, and TensorFlow/Keras.
   
2. **Data Analysis and Visualization**: 
   - pandas, NumPy: For data preprocessing, cleaning, and exploration.
   - Matplotlib, Seaborn: For data visualization to understand trends and correlations.

3. **Machine Learning Frameworks**:
   - scikit-learn: For traditional machine learning models like decision trees, random forests, and support vector machines.
   - TensorFlow/Keras: For more advanced deep learning models if required.
   
4. **Hyperparameter Optimization**: 
   - GridSearchCV or RandomizedSearchCV from scikit-learn for tuning machine learning models.

5. **Version Control**: 
   - Git: For version control and collaboration on the project.
   
6. **Deployment Tools**: 
   - Docker (optional): To containerize the machine learning model for easy deployment in real-time production environments.
   - Flask or FastAPI: For serving the model through an API if real-time predictions are required.

### Precautions

1. **Data Quality**: 
   - Ensure that the dataset is free of significant noise, missing values, or outliers. These can drastically affect the accuracy of the model.
   
2. **Overfitting**: 
   - Carefully monitor the performance of the machine learning model to avoid overfitting. Overfitting occurs when a model learns the training data too well but fails to generalize to new data.

3. **Data Leakage**: 
   - Avoid including future information in the training set that would not be available at the time of prediction. This can falsely inflate the model’s performance during evaluation.

4. **Ethical and Environmental Considerations**: 
   - While focusing on productivity improvements, ensure that any AI-driven optimizations do not lead to excessive resource usage (e.g., excessive energy consumption in the production process) or compromise worker safety.
   
5. **Model Interpretability**: 
   - Choose models that allow for interpretability, especially in an industrial setting. Being able to explain how input parameters affect output can be crucial in a production environment.

### Dataset Conclusions

1. **Dataset Overview**: 
   The dataset contains multiple input parameters that impact the quality of aluminum wire rods, such as chemical composition, casting speed, and emulsion conditions. The target variables include UTS (Ultimate Tensile Strength), elongation, conductivity, and rod quality (classified as 'Good' or 'Bad').

2. **Key Features**: 
   Parameters like casting temperature, cooling water temperature, and emulsion pressure appear to be closely related to the physical properties of the wire rods. These features need to be carefully evaluated for their correlation with the target variables.

3. **Target Variables**: 
   - UTS, elongation, and conductivity are numerical targets that can be predicted using regression models.
   - Rod quality (Good/Bad) is a classification target that can be modeled using classification algorithms like logistic regression, decision trees, or neural networks.

4. **Data Distribution**: 
   Initial inspection of the dataset indicates that the rod quality classes are relatively balanced. However, further exploration is required to confirm this and address any imbalance if found.

5. **Potential Challenges**: 
   - The dataset includes several dynamic parameters that interact with each other in complex ways. This could make feature selection challenging.
   - There may be a need to normalize or scale some of the features, such as temperature and pressure, to improve the performance of certain machine learning algorithms.

### Conclusion

By leveraging AI/ML techniques, this project seeks to transform aluminum wire rod production by enabling more accurate prediction of key physical properties and allowing real-time adjustments to process parameters. This will not only improve product quality but also enhance productivity and operational efficiency. The success of this project depends on careful data preprocessing, appropriate model selection, and the integration of the model into a real-time production environment for continuous quality control.
