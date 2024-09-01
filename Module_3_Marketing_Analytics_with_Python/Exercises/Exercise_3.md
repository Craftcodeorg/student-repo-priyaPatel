# Marketing Analytics with Python

## Exercise 3: Automated Performance Report Generation

### Problem Statement
You are tasked with creating an automated performance report for a healthcare marketing campaign that recently concluded. The report should summarize key metrics such as Return on Investment (ROI), Conversion Rate, and Customer Engagement for the campaign. You will write a Python script that generates this report in CSV format using the Pandas library.

The data for the campaign is provided in the following format:

| Campaign | Cost | Revenue | Clicks | Appointments |
|----------|------|---------|--------|--------------|
| Ad1      | 1000 | 5000    | 200    | 50           |
| Ad2      | 1500 | 7000    | 300    | 70           |
| Ad3      | 2000 | 3000    | 150    | 20           |

Your script should calculate the following metrics:
- **ROI**: \((\text{Revenue} - \text{Cost}) / \text{Cost} \times 100\)
- **Conversion Rate**: \(\text{Appointments} / \text{Clicks} \times 100\)
- **Customer Engagement**: \(\text{Clicks} / \text{Cost}\)

Finally, the script should save the report in a CSV file named `marketing_performance_report.csv`.

### Fill-in-the-Blank Starter Code
```python
import pandas as pd

# Sample data for the marketing campaigns
data = {
    'Campaign': ['Ad1', 'Ad2', 'Ad3'],
    'Cost': [1000, 1500, 2000],
    'Revenue': [5000, 7000, 3000],
    'Clicks': [200, 300, 150],
    'Appointments': [50, 70, 20]
}

# Create a DataFrame
df = pd.DataFrame(data)

# Calculate ROI
df['ROI'] = (df['Revenue'] - df['Cost']) / df['Cost'] * 100

# Calculate Conversion Rate
df['Conversion Rate'] = _______ / _______ * 100

# Calculate Customer Engagement
df['Customer Engagement'] = _______ / _______

# Save the report to CSV
df.to_csv('marketing_performance_report.csv', index=False)

print("Performance report generated successfully!")
```

### Hints
1. **For Conversion Rate**: Remember that you need to divide the number of appointments by the total clicks for each campaign.
2. **For Customer Engagement**: Think about how you can measure how effectively your spending is driving clicks.
3. **CSV Output**: Ensure you have set `index=False` when saving your DataFrame to avoid writing row indices in your CSV file.

### Expected Outcome
Upon completing this exercise, you should have a functional Python script that calculates and outputs key marketing metrics for the healthcare campaign into a CSV file. The filled-in code should demonstrate a clear understanding of how to manipulate data using Pandas and apply the concepts discussed in the lecture. Your final solution should include appropriate error handling (e.g., checking for division by zero) and be well-commented to explain each step of your calculations.

### Integration
This exercise is structured to facilitate your understanding of how to apply Python for marketing analytics. It aligns with your career goals as a Marketing Data Analyst and incorporates your interests in data visualization and marketing analytics. By completing this exercise, you will enhance your skills in using real-world marketing data projects and contribute to your portfolio of data visualization projects.