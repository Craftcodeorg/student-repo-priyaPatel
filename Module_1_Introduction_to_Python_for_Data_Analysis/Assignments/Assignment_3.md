### Assignment: Converting Marketing Data to a Pandas DataFrame and Performing Basic Statistical Analysis

#### Problem Statement:
As a Marketing Data Analyst in the healthcare sector, you are tasked with analyzing the performance of various marketing campaigns. Your goal is to convert a list of marketing campaign data into a Pandas DataFrame and perform basic statistical analysis to derive insights such as average ROI and the number of successful campaigns based on a defined threshold. This will help your team make informed decisions about future marketing strategies.

#### Starter Code:
Below is the starter code that sets up the environment for your analysis. You will need to complete the code by adding functionality to convert the list to a DataFrame and perform the required statistical analysis.

```python
import pandas as pd

# Sample marketing data: List of dictionaries containing campaign details
marketing_data = [
    {"Campaign": "Campaign A", "ROI": 150, "CTR": 0.05},
    {"Campaign": "Campaign B", "ROI": 200, "CTR": 0.07},
    {"Campaign": "Campaign C", "ROI": 90, "CTR": 0.03},
    {"Campaign": "Campaign D", "ROI": 120, "CTR": 0.06},
]

# Step 1: Convert the marketing data list to a Pandas DataFrame
def create_dataframe(data):
    # Your code here
    df = pd.DataFrame(data)
    return df

# Step 2: Perform basic statistical analysis
def analyze_campaigns(df):
    # Calculate average ROI
    average_roi = df['ROI'].mean()
    
    # Define a threshold for successful campaigns (e.g., ROI greater than 100)
    success_threshold = 100
    successful_campaigns = df[df['ROI'] > success_threshold]

    # Return results
    return average_roi, successful_campaigns

# Create DataFrame from marketing data
df_marketing = create_dataframe(marketing_data)

# Analyze the campaigns
average_roi, successful_campaigns = analyze_campaigns(df_marketing)

# Output results
print(f"Average ROI: {average_roi}")
print("Successful Campaigns:")
print(successful_campaigns)
```

#### Detailed Instructions:
1. **Step 1**: Complete the `create_dataframe` function by using `pd.DataFrame(data)` to convert the list of marketing data into a Pandas DataFrame. Ensure that the function returns the DataFrame.

2. **Step 2**: Inside the `analyze_campaigns` function, calculate the average ROI using `df['ROI'].mean()`. Define a threshold for successful campaigns (e.g., ROI greater than 100) and filter the DataFrame to find all campaigns that meet this criterion.

3. **Output**: Ensure that your output displays the average ROI and lists all successful campaigns with their details.

#### Criteria for Success and Evaluation:
- **Correctness**: The code must accurately convert the list to a DataFrame and perform the statistical analysis as specified.
- **Code Quality**: The code should be clean, well-documented with comments explaining each step, and follow best coding practices.
- **Output Clarity**: The output should be formatted in a clear and user-friendly manner, making it easy to understand the results of the analysis.

By completing this assignment, you will reinforce your understanding of Python's basic data types and structures while applying them in a real-world healthcare marketing context. This experience will contribute significantly to your goal of becoming a proficient Marketing Data Analyst.