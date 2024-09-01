# Assignment: Automated Weekly Performance Reports in Healthcare Marketing

## Problem Statement
As a Marketing Data Analyst in the healthcare sector, you are tasked with creating an automated script that generates weekly performance reports based on data scraped from your digital marketing campaigns. Your report should include key metrics such as Return on Investment (ROI) and Conversion Rates, which are essential for assessing the effectiveness of your campaigns. This assignment will help you apply the concepts learned in the lecture on analyzing marketing campaign performance using Python.

## Starter Code
Below is a basic framework for your script. You will need to modify and expand upon this code to complete the assignment.

```python
import pandas as pd
import matplotlib.pyplot as plt

# Sample scraped data (you will replace this with actual scraped data)
data = {
    'Campaign': ['Ad1', 'Ad2', 'Ad3'],
    'Cost': [1000, 1500, 2000],
    'Revenue': [5000, 7000, 3000],
    'Clicks': [200, 300, 150],  # Number of clicks for each campaign
    'Conversions': [50, 70, 30]  # Number of successful conversions (e.g., appointments booked)
}

# Create DataFrame
df = pd.DataFrame(data)

# Step 1: Calculate ROI and Conversion Rate
df['ROI'] = (df['Revenue'] - df['Cost']) / df['Cost'] * 100
df['Conversion Rate'] = df['Conversions'] / df['Clicks'] * 100

# Step 2: Visualize the results
plt.figure(figsize=(10, 5))

# Create a bar chart for ROI
plt.subplot(1, 2, 1)
plt.bar(df['Campaign'], df['ROI'], color='skyblue')
plt.title('ROI of Marketing Campaigns')
plt.xlabel('Campaign')
plt.ylabel('ROI (%)')

# Create a bar chart for Conversion Rates
plt.subplot(1, 2, 2)
plt.bar(df['Campaign'], df['Conversion Rate'], color='lightgreen')
plt.title('Conversion Rates of Marketing Campaigns')
plt.xlabel('Campaign')
plt.ylabel('Conversion Rate (%)')

plt.tight_layout()
plt.show()

# Step 3: Save the report to a CSV file
df.to_csv('weekly_performance_report.csv', index=False)
```

## Detailed Instructions
1. **Data Scraping**: Replace the sample data in the `data` dictionary with actual data scraped from your marketing campaigns. You can use libraries such as BeautifulSoup or Scrapy to scrape data from relevant websites or APIs.

2. **Calculate Additional Metrics**: Add calculations for other relevant metrics such as Click-Through Rate (CTR) and Customer Engagement. Modify the DataFrame to include these new metrics:
   - **CTR**: Calculate as `Clicks / Impressions` (you will need to add an `Impressions` column to your data).
   - **Customer Engagement**: You may define this based on your specific needs (e.g., number of repeat visits).

3. **Enhance Visualization**: Improve the visualizations by adding labels, legends, and customizing colors. Consider using different types of plots (like pie charts or line graphs) to represent various metrics effectively.

4. **Generate Reports**: Instead of just saving the report as a CSV file, create a more comprehensive report using libraries like ReportLab or Matplotlib to generate PDF reports that include visualizations and key insights.

5. **Automate the Script**: Finally, automate the execution of this script to run weekly using a task scheduler (like cron jobs on Unix-based systems or Task Scheduler on Windows).

## Criteria for Success and Evaluation
Your submission will be evaluated based on the following criteria:
- **Correctness**: The script accurately calculates ROI, Conversion Rates, and any additional metrics you choose to include.
- **Code Quality**: The code is clean, well-structured, and follows best practices (including comments and documentation).
- **Visualization**: The visualizations are clear, informative, and enhance the understanding of the data.
- **Report Generation**: The final report is comprehensive and presents data in a user-friendly format.
- **Automation**: The script demonstrates an understanding of how to automate tasks effectively.

By completing this assignment, you will gain hands-on experience with Python for marketing analytics and develop skills that are directly applicable to your career goals in healthcare marketing.