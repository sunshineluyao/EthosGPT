
# Traditional_vs_Secular and Survival_vs_SelfExpression Indices: Methodology and Implementation

This document provides a comprehensive overview of the methodology used to generate the **Traditional_vs_Secular** and **Survival_vs_SelfExpression** indices from survey data. The indices are derived from responses to key cultural questions, processed through standard statistical techniques. This document includes the exact survey questions, response formats, and detailed processing steps to ensure transparency and explainability.

---

## Table 1: Survey Questions and Prompts

The following questions were used to construct the cultural indices. Each question is accompanied by the exact prompt and response formatting instructions used during data collection.

| **ID**  | **Survey Question**                        | **Question Prompt with Response Formatting Instructions**                                                                                                                                                     |
|---------|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **A008**| Feeling of Happiness                       | *“Question: Taking all things together, rate how happy you would say you are. Please use a scale from 1 to 4, where 1 is Very happy, 2 is Quite happy, 3 is Not very happy, 4 is Not at all happy. Your score:”* |
| **A165**| Trust in People                            | *“Question: Generally speaking, would you say that most people can be trusted (option A) or that you need to be very careful in dealing with people (option B)? Your response (A or B):”*                       |
| **E018**| Respect for Authority                      | *“Question: If greater respect for authority takes place in the near future, do you think it would be a good thing, a bad thing, or you don’t mind? Reply 1 (Good), 2 (Don’t Mind), or 3 (Bad). Your answer:”*   |
| **E025**| Petition Signing Experience                | *“Question: Please tell me whether you have signed a petition (option A), might do it (option B), or would never do it (option C). Your response (A, B, or C):”*                                                |
| **F063**| Importance of God                          | *“Question: How important is God in your life? Rate on a scale from 1 (Not at all important) to 10 (Very important). Your score number:”*                                                                       |
| **F118**| Justifiability of Homosexuality            | *“Question: How justifiable do you think homosexuality is? Rate on a scale from 1 (Never justifiable) to 10 (Always justifiable). Your score number:”*                                                         |
| **F120**| Justifiability of Abortion                 | *“Question: How justifiable do you think abortion is? Rate on a scale from 1 (Never justifiable) to 10 (Always justifiable). Your score number:”*                                                              |
| **G006**| Pride of Nationality                       | *“Question: How proud are you to be your nationality? Rate on a scale from 1 (Very proud) to 4 (Not at all proud). Your score number:”*                                                                         |
| **Y002**| Post-Materialist Index                     | *“Question: Among the following goals, which do you consider most important? Respond with two numbers separated by a comma: 1 (Order), 2 (Say in Government), 3 (Prices), 4 (Freedom of Speech).”*             |
| **Y003**| Autonomy Index                             | *“Question: Which qualities should children be encouraged to learn? Choose up to 5 qualities: Independence, Hard work, Imagination, Respect, Religious faith, Obedience, etc. Your five choices:”*            |

### Numeric Transformation for Explainability

- **Textual responses (e.g., Yes/No or categorical options)** are converted into numeric values. For example:
  - **E025**: Signed petition (A) = 1, Might do it (B) = 0.5, Never (C) = 0.
  - **Y002**: Higher emphasis on freedom-related options (e.g., 2, 4) aligns with self-expression values.
  - **Y003**: Responses favoring autonomy-related qualities align positively with self-expression.

---

## Indices and Numeric Transformation

The two indices are calculated using Principal Component Analysis (PCA) on subsets of the survey questions. Their interpretations are as follows:

### **Traditional_vs_Secular Index**
- **Variables**: Q1 (Importance of God), Q2 (Obedience vs. Independence), Q3 (Abortion Justifiability), Q4 (National Pride), Q5 (Respect for Authority).
- **Interpretation**:
  - Negative values → **Traditional values**: Strong emphasis on religion, authority, and nationalism.
  - Positive values → **Secular values**: Rational outlooks, less emphasis on tradition.
- **Axis Representation**: On the y-axis of cultural maps.

### **Survival_vs_SelfExpression Index**
- **Variables**: Q6 (Economic Security), Q7 (Happiness), Q8 (Homosexuality Justifiability), Q9 (Petition Signing), Q10 (Trust in People).
- **Interpretation**:
  - Negative values → **Survival values**: Focus on economic and physical security.
  - Positive values → **Self-expression values**: Emphasis on tolerance, happiness, and personal empowerment.
- **Axis Representation**: On the x-axis of cultural maps.

---

## Data Processing Workflow

### Step 1: Preprocessing
- **Clean Data**: Handle missing responses and encode categorical values.
- **Aggregate Data**: Compute national-level means where applicable.

#### Example (Preprocessed Data)

| **Country** | **Q1** | **Q2** | **Q3** | **Q4** | **Q5** | **Q6** | **Q7** | **Q8** | **Q9** | **Q10** |
|-------------|--------|--------|--------|--------|--------|--------|--------|--------|--------|---------|
| Country A   | 8.5    | 1      | 2      | 3.5    | 3      | 1      | 3.8    | 1.2    | 0.2    | 2.5     |
| Country B   | 3.2    | 0      | 8.5    | 1.5    | 1.8    | 0      | 1.2    | 8.4    | 1.0    | 7.8     |

---

### Step 2: Factor Analysis
Perform PCA to reduce dimensions:
- **Traditional_vs_Secular Index**: Eigenvector of Q1-Q5.
- **Survival_vs_SelfExpression Index**: Eigenvector of Q6-Q10.

#### Example (Factor Scores)

| **Country** | **Traditional_vs_Secular** | **Survival_vs_SelfExpression** |
|-------------|----------------------------|--------------------------------|
| Country A   | 0.85                       | -0.75                         |
| Country B   | -1.25                      | 1.45                          |

---

### Step 3: Normalize Indices
Standardize scores to z-scores:
\[
F'_{ik} = \frac{F_{ik} - \mu_{F_k}}{\sigma_{F_k}}
\]

---

## Example Cases

| **Case**           | **Traditional_vs_Secular** | **Survival_vs_SelfExpression** | **Description**                                                                 |
|---------------------|---------------------------|--------------------------------|---------------------------------------------------------------------------------|
| **Case 1**: High Tradition, Low Survival  | -1.8                          | -0.9                             | Religious, nationalist, and focused on economic security.                       |
| **Case 2**: Low Tradition, High SelfExp   | 1.5                           | 1.7                              | Secular and progressive, with high self-expression values.                      |
| **Case 3**: Mixed Values                  | 0.1                           | 0.3                              | Balanced mix of traditional and self-expression characteristics.                |
| **Case 4**: High Tradition, High SelfExp  | -1.2                          | 1.1                              | Strong tradition, but also high emphasis on personal and cultural self-expression.|

---

This detailed methodology ensures clarity and consistency in deriving the indices and interpreting results.
##  To replicate the Inglehart–Welzel Cultural Map using the World Values Survey (WVS) Wave 7 data, follow these steps:

**1. Download the WVS Wave 7 Data and Codebook:**

- Visit the [WVS Wave 7 Documentation page](https://www.worldvaluessurvey.org/WVSDocumentationWV7.jsp).
- Download the "WVS Cross-National Wave 7 CSV v6.0.zip" file, which contains the survey data.
- Download the corresponding codebook to understand the variables and their coding.

**2. Set Up Your Environment:**

- Ensure you have Python installed on your system.
- Install the necessary libraries by running:

  ```bash
  pip install pandas numpy scikit-learn matplotlib seaborn
  ```

**3. Extract and Load the Data:**

- Unzip the downloaded "WVS Cross-National Wave 7 CSV v6.0.zip" file to access the CSV data file.
- Load the data into a pandas DataFrame:

  ```python
  import pandas as pd

  # Load the dataset
  df = pd.read_csv('WVS_Cross-National_Wave_7_csv_v6_0.csv')

  # Display the first few rows
  print(df.head())
  ```

**4. Identify and Select Relevant Variables:**

- Based on the codebook, identify the variables corresponding to the cultural dimensions:

  - `A008`: Feeling of Happiness
  - `A165`: Trust in People
  - `E018`: Respect for Authority
  - `E025`: Petition Signing Experience
  - `F063`: Importance of God
  - `F118`: Justifiability of Homosexuality
  - `F120`: Justifiability of Abortion
  - `G006`: Pride of Nationality
  - `Y002`: Post-Materialist Index
  - `Y003`: Autonomy Index

- Create a DataFrame with these selected columns:

  ```python
  # List of relevant columns
  relevant_columns = ['A008', 'A165', 'E018', 'E025', 'F063', 'F118', 'F120', 'G006', 'Y002', 'Y003']

  # Select relevant columns
  data = df[relevant_columns]
  ```

**5. Preprocess the Data:**

- Handle missing values and standardize responses:

  ```python
  from sklearn.impute import SimpleImputer
  from sklearn.preprocessing import StandardScaler

  # Handle missing values by imputing with the mean
  imputer = SimpleImputer(strategy='mean')
  data_imputed = imputer.fit_transform(data)

  # Standardize the data
  scaler = StandardScaler()
  data_standardized = scaler.fit_transform(data_imputed)
  ```

**6. Perform Principal Component Analysis (PCA):**

- Apply PCA to extract the main components representing the cultural dimensions:

  ```python
  from sklearn.decomposition import PCA

  # Perform PCA
  pca = PCA(n_components=2)
  principal_components = pca.fit_transform(data_standardized)

  # Create a DataFrame with the principal components
  pca_df = pd.DataFrame(data=principal_components, columns=['Secular-Rational', 'Self-Expression'])
  ```

**7. Aggregate Scores by Country:**

- Assuming your original DataFrame `df` contains a 'Country' column, compute the mean scores for each country on the two dimensions:

  ```python
  # Add principal components to the original DataFrame
  df['Secular-Rational'] = pca_df['Secular-Rational']
  df['Self-Expression'] = pca_df['Self-Expression']

  # Group by country and calculate mean scores
  country_scores = df.groupby('Country')[['Secular-Rational', 'Self-Expression']].mean().reset_index()
  ```

**8. Plot the Cultural Map:**

- Visualize the cultural map using a scatter plot:

  ```python
  import matplotlib.pyplot as plt
  import seaborn as sns

  plt.figure(figsize=(12, 8))
  sns.scatterplot(data=country_scores, x='Self-Expression', y='Secular-Rational', hue='Country', s=100)

  # Annotate each point with the country name
  for i in range(country_scores.shape[0]):
      plt.text(x=country_scores['Self-Expression'][i] + 0.02,
               y=country_scores['Secular-Rational'][i],
               s=country_scores['Country'][i],
               fontdict=dict(color='black', size=10),
               bbox=dict(facecolor='yellow', alpha=0.5))

  plt.title('Inglehart–Welzel Cultural Map')
  plt.xlabel('Survival vs. Self-Expression Values')
  plt.ylabel('Traditional vs. Secular-Rational Values')
  plt.legend(loc='upper right', bbox_to_anchor=(1.15, 1))
  plt.grid(True)
  plt.show()
  ```

**9. Interpret the Map:**

- Analyze the placement of countries to understand cultural similarities and differences. Compare your results with the official WVS cultural map for validation.

**Note:** Ensure that the selected survey questions and their coding align with the theoretical constructs of the Inglehart–Welzel Cultural Map. Refer to the [World Values Survey documentation](https://www.worldvaluessurvey.org/WVSContents.jsp?CMSID=Findings) for detailed information on variable selection and coding. 


--

