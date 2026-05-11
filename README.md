# [cite_start]Agricultural Crop Health Classification via Drone Analytics [cite: 3]

## [cite_start]Project Overview [cite: 3]
[cite_start]This project focuses on predicting crop health status, specifically distinguishing between healthy and unhealthy crops, by using simulated multispectral and environmental data captured by drones[cite: 3, 23]. [cite_start]By leveraging machine learning, this tool supports precision agriculture, helping farmers identify stressed crops early to optimize irrigation and fertilizer use[cite: 4, 24].

## [cite_start]Key Features [cite: 5, 25]
* [cite_start]**Intelligent Feature Engineering:** Specialized indices, such as Thermal_Moisture and Green_Stress (NDVI/Chlorophyll ratio), were created to better capture plant physiology[cite: 5, 25].
* [cite_start]**Advanced Data Balancing:** ADASYN (Adaptive Synthetic Sampling) was implemented to address class imbalance, ensuring the model identifies unhealthy crops as effectively as healthy ones[cite: 6, 26].
* [cite_start]**Robust Preprocessing:** Z-Score filtering was used for outlier removal, and RobustScaler was utilized to manage features with high variance[cite: 7, 27].
* [cite_start]**Automated Feature Selection:** A "One-Pass" Random Forest importance ranking was used to identify the 12 most predictive variables[cite: 8, 28].

## [cite_start]Tech Stack [cite: 9, 29]
* [cite_start]**Language:** Python [cite: 9]
* **Libraries:**
    * [cite_start]**scikit-learn:** Robust scaling and Random Forest Classifier [cite: 9]
    * [cite_start]**imblearn:** Synthetic data generation via ADASYN [cite: 10]
    * [cite_start]**pandas/numpy:** High-performance data manipulation [cite: 10]
    * [cite_start]**seaborn/matplotlib:** Statistical data visualization [cite: 10]

## [cite_start]Pipeline Workflow [cite: 11]
1. [cite_start]**Cleaning:** Removal of non-predictive spatial data, including GPS and bounding boxes, and imputation of missing values[cite: 11, 30].
2. [cite_start]**Engineering:** Generation of interaction terms reflecting biological stress markers[cite: 12, 31].
3. [cite_start]**Balancing:** Application of ADASYN to equalize crop health label representation[cite: 13, 32].
4. [cite_start]**Modeling:** Training a Random Forest Classifier with restricted depth to maintain high predictive power while preventing overfitting[cite: 14, 33].
5. [cite_start]**Evaluation:** Performance analysis through precision-recall reports and confusion matrices[cite: 15, 34].

## [cite_start]Performance and Insights [cite: 16, 35]
[cite_start]The model achieved an overall accuracy of 0.63, demonstrating a balanced ability to distinguish between classes[cite: 16, 35].

### [cite_start]Key Insights [cite: 17]
* [cite_start]**Feature Importance:** Soil_Moisture, NDVI, and the engineered Thermal_Moisture index were consistently ranked as primary drivers of health status[cite: 17, 36].
* [cite_start]**Confusion Matrix:** The model demonstrates high stability, with nearly equal recall for healthy and unhealthy classes, providing a reliable baseline for drone-based scanning[cite: 18, 37].

## [cite_start]Visualizations [cite: 19]
[cite_start]The project includes the following visual representations[cite: 19]:
* [cite_start]**Confusion Matrix:** A visual representation of false positives versus true positives[cite: 20, 38].
* [cite_start]**Feature Importance Plot:** A horizontal bar chart showcasing the 12 most influential environmental and spectral sensors[cite: 21, 39].

---
