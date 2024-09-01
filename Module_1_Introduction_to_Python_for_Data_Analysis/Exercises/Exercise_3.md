### Module Title: Introduction to Python for Data Analysis ###

### Exercise 3: Load a CSV file using Pandas ###

#### 1. Problem Statement:
As a Marketing Data Analyst in the Healthcare Marketing industry, you are tasked with analyzing the performance of various marketing campaigns. You have been provided with a CSV file named `marketing_campaigns.csv` that contains data on different campaigns, including their ROI, CTR, and the number of leads generated. Your objective is to load this CSV file using Pandas, explore the data, and extract insights that can help improve future campaigns.

The CSV file has the following structure:
```
Campaign_Name,ROI,CTR,Leads
Campaign A,150,0.05,300
Campaign B,200,0.07,450
Campaign C,100,0.03,200
```

Your task is to:
1. Load the CSV file using Pandas.
2. Print the first five rows of the DataFrame.
3. Calculate the average ROI and CTR across all campaigns.
4. Identify which campaign generated the most leads.

#### 2. Fill-in-the-Blank Starter Code:
```python
import pandas as pd

# Load the CSV file into a DataFrame
df = pd.read_csv('__________')  # Fill in the blank with the path to your CSV file

# Display the first five rows of the DataFrame
print(df.head())

# Calculate the average ROI
average_roi = df['ROI'].mean()  # Calculate average ROI
print(f"Average ROI: {average_roi}")

# Calculate the average CTR
average_ctr = df['CTR'].mean()  # Calculate average CTR
print(f"Average CTR: {average_ctr}")

# Identify the campaign with the most leads
max_leads_campaign = df.loc[df['Leads'].idxmax(), 'Campaign_Name']  # Find campaign with max leads
print(f"Campaign with most leads: {max_leads_campaign}")
```

#### 3. Hints:
- Make sure to import the Pandas library at the beginning of your code.
- Use `pd.read_csv()` to load your CSV file. Ensure you provide the correct path to the file.
- To calculate averages, remember to use the `.mean()` method on the respective columns of your DataFrame.
- Use `.idxmax()` to find the index of the maximum value in a column, and then use `.loc[]` to access that row in the DataFrame.

#### 4. Expected Outcome:
Upon completing this exercise, you should have a fully functional Python script that:
- Successfully loads data from a CSV file into a Pandas DataFrame.
- Displays the first five rows of the DataFrame for an overview of your data.
- Computes and prints the average ROI and CTR for all marketing campaigns.
- Identifies and prints the name of the campaign that generated the most leads.

Your final solution should follow best practices such as including error handling (e.g., checking if the file exists) and should be well-commented to explain each step clearly. This exercise will help you apply your knowledge of basic data types and structures in Python while working with real-world marketing data relevant to your career goals in Healthcare Marketing.