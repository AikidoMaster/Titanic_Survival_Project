

# Titanic EDA (Exploratory Data Analysis)

## Project Overview

This project involves performing exploratory data analysis (EDA) on the Titanic dataset. The goal of the analysis is to identify patterns and relationships within the data that could help predict passenger survival. The dataset used in this analysis is the classic Titanic dataset, which includes information about the passengers, such as their age, sex, class, fare, and whether they survived.

## Project Structure

The project is organized into the following steps:

1. **Loading the Data**: 
   - The dataset (`train.csv`) is loaded into a Pandas DataFrame.
   - The first few rows of the dataset are displayed to get an overview of the data.

2. **Handling Missing Values**:
   - The missing values in the dataset are identified.
   - The `Age` and `Cabin` columns have a significant number of missing values, and strategies for handling these may be considered in further analysis.

3. **Visualizations**:
   - Several visualizations are created to explore relationships between variables:
     - **Countplot**: Shows the count of passengers by sex and survival status.
     - **Heatmap**: Displays the relationship between passenger class (`Pclass`) and survival status.
     - **Violinplot**: Illustrates the distribution of age by sex and survival status.
     - **Factorplot**: Explores the relationship between family size (`Family_Size`) and survival, as well as the effect of being alone (`Alone`).
     - **Barplot**: Examines the survival rates across different fare ranges (`Fare_Range`).
     - **Countplot by Embarked and Pclass**: Shows survival rates based on the port of embarkation and passenger class.

4. **Feature Engineering**:
   - Two new features are created:
     - `Family_Size`: A combination of `SibSp` (siblings/spouses aboard) and `Parch` (parents/children aboard).
     - `Alone`: A binary feature indicating if a passenger is alone (no family aboard).

5. **Conclusion**:
   - Several columns are identified as not contributing much to the outcome and are considered for removal in further modeling:
     - `PassengerId`, `Name`, `Ticket`, `Cabin` (as they are mostly strings or have too many unique values).
     - `Age`, `Fare` (considering that ranges might be more meaningful for analysis).

## Dependencies

To run this analysis, you will need the following Python libraries:

- pandas
- seaborn
- matplotlib

You can install the necessary packages using pip:

```bash
pip install pandas seaborn matplotlib
```

## Running the Analysis

1. Clone the repository or download the project files.
2. Ensure that the Titanic dataset (`train.csv`) is in the working directory.
3. Open the Jupyter notebook (`Titanic_EDA_Rohit_Ganguly.ipynb`).
4. Run the cells sequentially to execute the analysis.

## Conclusion

This EDA has provided insights into which features might be useful for predictive modeling. Future steps could include model building and evaluation based on these findings.

