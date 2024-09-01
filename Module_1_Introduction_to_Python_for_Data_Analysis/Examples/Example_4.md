# Module Title: Introduction to Python for Data Analysis

## Example 4: Basic Data Manipulation with Pandas

### 1. Introduction
In this section, we will explore "Example 4: Basic data manipulation with Pandas" as covered in the lecture titled "Introduction to Libraries: NumPy and Pandas." This example is particularly significant in the context of Healthcare Marketing, where analyzing customer engagement and campaign effectiveness is crucial for improving marketing strategies and outcomes.

Pandas is a powerful tool that allows marketers to manipulate and analyze structured data efficiently. By mastering data manipulation techniques using Pandas, you can automate the analysis of marketing campaigns, derive insights from healthcare consumer behavior, and ultimately enhance your decision-making process.

### 2. Code Snippet
Here is a well-commented code snippet that demonstrates basic data manipulation with Pandas. This example calculates the average engagement score of patients participating in a healthcare marketing campaign.

```python
import pandas as pd

# Sample data: Patient engagement scores from a recent marketing campaign
data = {
    'Patient ID': ['P1', 'P2', 'P3', 'P4'],
    'Engagement Score': [75, 80, 65, 90]
}

# Load data into a DataFrame
df = pd.DataFrame(data)

# Check for missing values in the DataFrame
if df.isnull().values.any():
    print("Warning: Missing values detected in the dataset.")

# Calculate the average engagement score
average_score = df['Engagement Score'].mean()

# Display the average engagement score
print(f"Average Engagement Score from DataFrame: {average_score:.2f}")
```

### 3. Explanation
Let's break down the code step-by-step:

1. **Importing Pandas**: The first line imports the Pandas library, which is essential for data manipulation.
   
2. **Creating Sample Data**: We define a dictionary called `data` containing `Patient ID` and their corresponding `Engagement Score`. This simulates a dataset you might encounter in healthcare marketing.

3. **Loading Data into a DataFrame**: The dictionary is converted into a Pandas DataFrame named `df`. DataFrames are versatile structures that allow for easy manipulation of tabular data.

4. **Checking for Missing Values**: We use the `isnull()` method to check if there are any missing values in the DataFrame. If any are found, a warning message is printed. This step is crucial for ensuring data quality before analysis.

5. **Calculating Average Engagement Score**: The `mean()` function calculates the average of the `Engagement Score` column, providing insight into overall patient engagement.

6. **Displaying Results**: Finally, we print the average engagement score formatted to two decimal places. This output helps marketers understand how well their campaign performed in engaging patients.

### 4. Application
In Healthcare Marketing, understanding patient engagement is vital for evaluating the effectiveness of marketing campaigns. By utilizing Pandas for data manipulation, healthcare marketers can:

- **Analyze Engagement Trends**: By calculating average engagement scores across different campaigns or demographics, marketers can identify which strategies are most effective in reaching patients.
  
- **Automate Reporting**: With automated scripts using Pandas, marketers can generate reports on patient engagement metrics regularly, saving time and reducing human error.

- **Make Informed Decisions**: Insights derived from data manipulation can guide future marketing strategies, ensuring that resources are allocated efficiently to maximize patient engagement and improve health outcomes.

### Conclusion
By mastering basic data manipulation with Pandas, you will enhance your ability to analyze healthcare marketing data effectively. This foundational knowledge will empower you to build interactive dashboards and automate reporting processes, ultimately advancing your career as a Marketing Data Analyst. In our next lecture, we will explore data visualization techniques using Matplotlib and Seaborn to complement your analytical skills.