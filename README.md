## Gun Violence

The following Python libraries were used:
`pandas`
`sklearn.model_selection`
`sklearn.ensemble`
`sklearn.metrics`
`sklearn.preprocessing`
`seaborn`
`matplotlib.pyplot`
`scipy.stats`
### Overview
The United States is infamous for the high frequency and severity of gun-related violent incidents. While this project cannot solve this problem, it can shed light on possible causes and make predictions that would aid the future prevention of such events. The project analyzes the number of lesgislative laws that protect against firearm violence by state and compares them with the number of shootings in each state. 

### Features
**Data Integration**: Gun violence, Mortality, and Firearm Provision data frames have been merged using state and years as keys to analyze the correlation between the number of the laws impemented in each state to protect against gun violence with the number of incidents and rate of deaths over the years. 

**Data Cleaning**: Null values have been removed and the keys have been standardized to allow for easy data integration.

**Modeling**: Random Forest Classifier is used to identify high risk locations for an original and regularized model.

**Evaluation**: A Classification Report and ROC-AUC score is used to evaluate model performance.
