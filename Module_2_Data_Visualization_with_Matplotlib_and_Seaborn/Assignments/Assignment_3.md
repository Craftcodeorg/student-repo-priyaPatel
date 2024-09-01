### Assignment: Develop a Heatmap to Display Correlations Between Marketing Metrics

#### Problem Statement
In the healthcare marketing industry, understanding the relationships between various marketing metrics is crucial for optimizing campaign performance. For this assignment, you will create a heatmap that visualizes the correlations between different marketing metrics, such as ad spend, impressions, clicks, and conversions. This task will help you apply the visualization concepts learned in the lecture and provide insights into how these metrics interact with each other.

#### Starter Code
Below is a basic code framework that you will expand upon to create the heatmap. The starter code includes sample data representing different marketing metrics and sets up the environment for generating the heatmap using Seaborn.

```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd

# Sample Data: Marketing Metrics
data = {
    'Ad Spend': [1000, 1500, 2000, 2500, 3000],
    'Impressions': [10000, 15000, 20000, 25000, 30000],
    'Clicks': [100, 150, 200, 250, 300],
    'Conversions': [10, 15, 20, 25, 30]
}

# Create DataFrame
df = pd.DataFrame(data)

# Step 1: Calculate the correlation matrix
correlation_matrix = df.corr()

# Step 2: Create a heatmap using Seaborn
plt.figure(figsize=(8, 6))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt='.2f')
plt.title('Correlation Heatmap of Marketing Metrics')
plt.show()
```

#### Detailed Instructions
1. **Understanding the Data**: Review the sample data provided in the starter code. Each column represents a different marketing metric that you will analyze for correlations.

2. **Calculate Correlation Matrix**: 
   - The starter code already includes a line to calculate the correlation matrix using `df.corr()`. Ensure you understand how this function works and what it returns.

3. **Create the Heatmap**:
   - The code snippet provided uses Seaborn to create a heatmap from the correlation matrix. 
   - Modify the `plt.figure(figsize=(8, 6))` line to adjust the size of the heatmap if necessary.
   - The `annot=True` parameter displays the correlation values on the heatmap. You can change `fmt='.2f'` to format the numbers differently if you prefer.

4. **Enhance Visualization**:
   - Add additional styling to your heatmap to improve its clarity and aesthetic appeal. Consider changing the color palette by modifying the `cmap` parameter (e.g., use `'viridis'` or `'Blues'`).
   - Experiment with other Seaborn features to make your heatmap more informative (e.g., adjusting line widths or adding labels).

5. **Interpret Results**:
   - After generating the heatmap, analyze the correlations between metrics. Write a brief summary (3-5 sentences) interpreting what the correlations mean for healthcare marketing strategies.

#### Criteria for Success and Evaluation
- **Accuracy**: The heatmap correctly displays the correlation coefficients between marketing metrics.
- **Code Quality**: The code is clean, well-structured, and includes comments explaining each step.
- **Visualization Quality**: The heatmap is visually appealing and easy to interpret.
- **Interpretation**: A clear summary is provided that accurately interprets the results of the heatmap in the context of healthcare marketing.

By completing this assignment, you will not only reinforce your understanding of data visualization but also enhance your skills in analyzing and interpreting marketing data—essential competencies for your career goal of becoming a Marketing Data Analyst in Healthcare Marketing.