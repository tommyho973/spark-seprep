### Assignment 5: Data Science 101

#### Title: Exploratory Data Analysis (EDA) and Hypothesis Testing on Less Common Datasets

#### Objective:
The objective of this assignment is to encourage students to explore and analyze datasets, perform Exploratory Data Analysis (EDA), frame hypotheses, and use data visualization to prove or disprove their hypotheses. Students will create a Jupyter notebook for their analysis.

#### Datasets to Choose From:

1. **Wine Quality Dataset:**
   - Dataset: [Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/wine+quality)
   - Description: Contains various physicochemical properties of red and white wine, and quality ratings.

2. **Forest Fires Dataset:**
   - Dataset: [Forest Fires Dataset](https://archive.ics.uci.edu/ml/datasets/forest+fires)
   - Description: Provides information on forest fires in Portugal, including meteorological and other factors.

3. **Bank Marketing Dataset:**
   - Dataset: [Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing)
   - Description: Focuses on a bank's marketing campaign, including client information and campaign outcomes.

4. **Absenteeism at Work Dataset:**
   - Dataset: [Absenteeism at Work Dataset](https://archive.ics.uci.edu/ml/datasets/Absenteeism+at+work)
   - Description: Examines factors contributing to absenteeism in a company, including personal and work-related variables.

5. **Online News Popularity Dataset:**
   - Dataset: [Online News Popularity Dataset](https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity)
   - Description: Analyzes the popularity of online news articles based on various features.

#### Assignment Tasks:

1. **Importing Data and Libraries:**
   - Use Python and Jupyter notebook to import the chosen dataset and necessary libraries (Pandas, NumPy, Matplotlib, Seaborn).

2. **Exploratory Data Analysis (EDA):**
   - Explore the dataset's structure, summary statistics, and distributions.
   - Visualize key features using appropriate plots (scatter plots, histograms, etc.).

3. **Hypothesis Formulation:**
   - Frame at least two hypotheses related to the dataset. For example:
     - "There is a correlation between alcohol content and wine quality."
     - "The day of the week influences absenteeism at work."

4. **Hypothesis Testing:**
   - Use statistical tests or visualizations to test the formulated hypotheses.
   - Discuss the results and draw conclusions based on the analysis.

5. **Documentation and Reporting:**
   - Document the entire analysis process, including code, explanations, and interpretations.
   - Summarize key findings in a clear and concise report.

#### Sample Jupyter Notebook Template:

```python
# Importing libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Importing the dataset
# Replace 'your_dataset_url' with the actual URL or file path
url = 'your_dataset_url'
df = pd.read_csv(url)

# Exploratory Data Analysis (EDA)
# Explore the dataset's structure and summary statistics

# Visualize key features using plots

# Hypothesis Formulation
# Formulate at least two hypotheses related to the dataset

# Hypothesis Testing
# Test the formulated hypotheses using statistical tests or visualizations

# Documentation and Reporting
# Document the entire analysis process, including code and explanations
# Summarize key findings in a clear and concise report
```

**Note:** Students should replace `your_dataset_url` with the actual URL or file path of their chosen dataset. 
##### Extra Credit : Additional analyses and inferences beyond the outlined tasks for a more comprehensive understanding.


#### How to Submit:
Create a fork of the repository, add a new branch for this assignment and then create a folder here [https://github.com/DS219/spark-seprep/tree/main/assignments/assignment5/](https://github.com/DS219/spark-seprep/tree/main/assignments/assignment5/) with your name, and add the dataset you choose and jupyter notebook in this folder. After adding it your fork, make a pull request to the upstream repository.
