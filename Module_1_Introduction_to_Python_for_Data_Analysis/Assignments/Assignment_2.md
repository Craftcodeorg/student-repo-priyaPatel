### Assignment: Develop a Function to Calculate the Average of Key Marketing Metrics

#### Problem Statement:
As a Marketing Data Analyst in the healthcare industry, understanding consumer behavior through data analysis is crucial for creating targeted marketing campaigns. In this assignment, you will develop a function that calculates the average of key marketing metrics from a list of consumer spending data. This exercise will reinforce your understanding of Python and its application in analyzing marketing data.

#### Starter Code:
Below is the starter code that sets up the environment for you to build upon. Your task is to complete the function `calculate_average_metrics` to compute the average spending and identify any spending values that exceed the average by more than 10%.

```python
# Starter code for calculating average marketing metrics

def calculate_average_metrics(spending_data):
    """
    This function calculates the average spending from a list of consumer spending data.
    It also identifies spending amounts that exceed the average by more than 10%.
    
    Parameters:
    spending_data (list): A list of consumer spending amounts.
    
    Returns:
    tuple: Average spending, List of high spenders
    """
    
    # Step 1: Calculate the average spending
    avg_spending = sum(spending_data) / len(spending_data)
    
    # Step 2: Identify spending amounts that exceed the average by more than 10%
    high_spenders = []
    for amount in spending_data:
        if amount > avg_spending * 1.1:
            high_spenders.append(amount)
    
    # Return results (students will need to format the output)
    return avg_spending, high_spenders

# Test the function with sample data
spending_data = [100, 150, 200, 250, 300]
average, high_spenders = calculate_average_metrics(spending_data)
print(f"Average Spending: {average}")
print(f"Spending Exceeding 10% Over Average: {high_spenders}")
```

#### Detailed Instructions:
1. **Calculate Average Spending**: Ensure that your function accurately computes the average spending from the `spending_data` list.
2. **Identify High Spenders**: Modify the loop to not only find amounts that exceed the average by 10% but also to return their respective indices in the original list.
3. **Enhance Output**: Format the output to provide clear feedback. For example, instead of just listing high spenders, include a message indicating how much they exceeded the average.
4. **Documentation**: Add comments to your code explaining each step clearly.

#### Criteria for Success and Evaluation:
- **Correctness**: The function should correctly calculate the average and identify high spenders based on the criteria provided.
- **Code Quality**: The code should be clean, well-organized, and include comments that enhance readability.
- **Output Formatting**: The output should be user-friendly and clearly convey the results of your analysis.

**Success Criteria:**
- The function correctly calculates the average spending and identifies amounts exceeding 10% over the average.
- The code is well-documented with clear comments.
- The output is formatted in a way that is easy to understand for stakeholders in healthcare marketing.

This assignment will help you practice your coding skills while applying them to real-world scenarios relevant to your career goals in healthcare marketing analytics. Good luck!