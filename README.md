**Agricultural Crop Health Classification via Drone Analytics***

**Project Overview**

This project focuses on predicting crop health status, specifically distinguishing between healthy and unhealthy crops, by using simulated multispectral and environmental data captured by drones. By leveraging machine learning, this tool supports precision agriculture, helping farmers identify stressed crops early to optimize irrigation and fertilizer use.


**Key Features** 


*Intelligent Feature Engineering*: Specialized indices, such as Thermal_Moisture and Green_Stress (NDVI/Chlorophyll ratio), were created to better capture plant physiology.


*Advanced Data Balancing*: ADASYN (Adaptive Synthetic Sampling) was implemented to address class imbalance, ensuring the model identifies unhealthy crops as effectively as healthy ones.


*Robust Preprocessing*: Z-Score filtering was used for outlier removal, and RobustScaler was utilized to manage features with high variance.


*Automated Feature Selection*: A "One-Pass" Random Forest importance ranking was used to identify the 12 most predictive variables.


**Tech Stack** 


*Language*: Python 


*Libraries*: * scikit-learn: Robust scaling and Random Forest Classifier 


*imblearn*: Synthetic data generation via ADASYN 


*pandas/numpy*: High-performance data manipulation 


*seaborn/matplotlib*: Statistical data visualization 


**Pipeline Workflow** 


*Cleaning*: Removal of non-predictive spatial data, including GPS and bounding boxes, and imputation of missing values.


*Engineering*: Generation of interaction terms reflecting biological stress markers.


*Balancing*: Application of ADASYN to equalize crop health label representation.


*Modeling*: Training a Random Forest Classifier with restricted depth to maintain high predictive power while preventing overfitting.


*Evaluation*: Performance analysis through precision-recall reports and confusion matrices.


**Performance and Insights** 

The model achieved an overall accuracy of 0.63, demonstrating a balanced ability to distinguish between classes.


**Key Insights** 


*Feature Importance*: Soil_Moisture, NDVI, and the engineered Thermal_Moisture index were consistently ranked as primary drivers of health status.


*Confusion Matrix*: The model demonstrates high stability, with nearly equal recall for healthy and unhealthy classes, providing a reliable baseline for drone-based scanning.


**Visualizations** 

The project includes the following visual representations:


*Confusion Matrix*: A visual representation of false positives versus true positives.


*Feature Importance Plot*: A horizontal bar chart showcasing the 12 most influential environmental and spectral sensors.
