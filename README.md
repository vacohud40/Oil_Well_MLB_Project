# Oil Well Profit Prediction: Maximizing Returns for New Well Development

## Project Description

This project focuses on developing a machine learning model to predict the volume of oil reserves in new wells across three different geological regions. The ultimate goal is to strategically select the most promising wells for development to maximize the overall profit for Sweet Lift Taxi company. The model is built using historical geological exploration data, which includes unique well identifiers and three key feature points.

## Analysis Goals

The primary objective of this analysis is to identify the region with the highest potential profit while simultaneously minimizing the risk of financial losses. This will be achieved through a multi-faceted approach:

* **Data Exploration and Preparation:** Thoroughly understanding the characteristics of the geological data for each region, identifying patterns, handling any inconsistencies, and preparing the data for robust model training.
* **Model Training and Evaluation:** Training a linear regression model independently for each of the three regions. The performance of each model will be rigorously evaluated using the Root Mean Squared Error (RMSE) for prediction quality and the average predicted reserves.
* **Profit Calculation and Risk Assessment:** Developing a function to calculate the potential profit based on predicted oil volumes, accounting for development budget and revenue per unit of product. Bootstrapping techniques will be utilized to simulate and estimate the distribution of profits for each region, enabling a comprehensive assessment of the risk of losses.
* **Optimal Region Selection:** Based on the calculated average profit and assessed risk of losses (targeting below 2.5%), the project will recommend the optimal region for new oil well development.

## Key Constants for Profit Calculation

The profit calculations and risk assessments are based on the following predefined business constants:

* **`BUDGET`**: $100,000,000 (for developing 200 wells)
* **`NUM_WELLS`**: 200 (Number of top wells to be developed in a selected region)
* **`REVENUE_PER_PRODUCT`**: $4,500 (Revenue per thousand barrels of oil, if the 'product' column represents thousands of barrels)
* **`SAMPLE_SIZE`**: 1000 (Number of bootstrap samples for profit distribution)
* **`SAMPLE_POINTS`**: 500 (Number of points used for the bootstrapping sample)
* **`STATE`**: `np.random.RandomState(12345)` (Fixed random state for reproducibility)

## Technologies Used

* **Python**
* **Pandas:** For efficient data loading, manipulation, and analysis of geological data.
* **NumPy:** For numerical operations, array manipulation, and statistical calculations, especially during bootstrapping.
* **Scikit-learn:** For machine learning model implementation (`LinearRegression`), data splitting (`train_test_split`), and evaluation metrics (`mean_squared_error`).
* **Matplotlib:** For creating static data visualizations, including pairplots, correlation heatmaps, and distributions.
* **Seaborn:** For enhancing the aesthetic quality and informativeness of statistical graphics.
* **Jupyter Notebook:** The primary environment for conducting the analysis, experimentation, and presenting findings.

## Dataset

The project utilizes geological exploration data from three distinct regions.

* **File Names:**
    * `geo_data_0.csv`: Data for Region 0.
    * `geo_data_1.csv`: Data for Region 1.
    * `geo_data_2.csv`: Data for Region 2.
* **Content:** Each dataset contains:
    * `id`: Unique well identifier.
    * `f0`, `f1`, `f2`: Three geological feature points.
    * `product`: The volume of oil reserves in the well (target variable).
* **Original Location (on training platform):** `/datasets/geo_data_0.csv`, `/datasets/geo_data_1.csv`, `/datasets/geo_data_2.csv`

