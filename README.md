## Gun Violence

### Overview
The United States is infamous for the high frequency and severity of gun-related violent incidents. While this project cannot solve this problem, it can shed light on possible causes and make predictions that would aid the future prevention of such events. The project analyzes the number of lesgislative laws that protect against firearm violence by state and compares them with the number of shootings in each state. 

### Requirements
`pandas`

`sklearn.model_selection`

`sklearn.ensemble`

`sklearn.metrics`

`sklearn.preprocessing`

`seaborn`

`matplotlib.pyplot`

`scipy.stats`

### Datasets
**<a href="https://www.kaggle.com/datasets/jboysen/state-firearms">Provisions</a>**: (Originally from the Department of Justice and found on Kaggle)

Contains the encoded laws against firearm violence by state and year and has lawtotal count.

**<a href="https://www.kaggle.com/datasets/jameslko/gun-violence-data">Gun Violence Data</a>**: (Originally from the Gun Violence Archrive and found on Kaggle)

Contains the number of people killed and injured in a gun violence incident by state and year.

**<a href="https://www.cdc.gov/nchs/pressroom/sosmap/firearm_mortality/firearm.htm">Mortality Rate</a>** (Found on the CDC website)

Contains the mortality rate and number of deaths by state and year.

### Features
**Data Integration**: Gun violence, Mortality, and Firearm Provision data frames have been merged using state and years as keys to analyze the correlation between the number of the laws impemented in each state to protect against gun violence with the number of incidents and rate of deaths over the years. 

**Data Cleaning**: Null values have been removed and the keys have been standardized to allow for easy data integration.

**Modeling**: Random Forest Classifier is used to identify high risk locations for an original and regularized model.

*  **Original Model:** Includes key features like lawtotal, RATE, n_killed, and n_injured.
*  **Regularized Model:** Focuses on reducing overfitting by evaluating feature importance.

**Evaluation**: A Classification Report and ROC-AUC score is used to evaluate model performance.

### Results
**High-Risk Locations:**
* Identified states and years with elevated risk based on gun violence trends.
* Highlighted states with consistently high high_risk_prob values for targeted interventions.
**Law Effectiveness:**
* Waiting periods showed a statistically significant impact in reducing high-risk probabilities.
* Other provisions, such as stricter age requirements, correlated weakly with reduced risks.

### Usage
Clone this repository:
* ```git clone https://github.com/rudrakshsimlote/gun-violence-dmg```
* Ensure all required datasets are in the project directory.
* Run the Jupyter Notebook files for preprocessing and analysis:
   * Data_Cleaning.ipynb: Cleans and prepares the datasets.
   * merging_data.ipynb: Merges the datasets, trains models, and evaluates predictions.

### Future Work
* **Mass Shootings Focus:** Build a separate model to predict high-severity incidents based on mass shooting-specific data.
* **Interactive Dashboard:** Create a Streamlit or Dash app to visualize high-risk locations and trends dynamically.

### Contributors
* **Rudraksh Simlote**
* **Aarya Shah**
* **Sandhya Ganesh**
