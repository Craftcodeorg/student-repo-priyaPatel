# Module Title: Data Visualization with Matplotlib and Seaborn

## Exercise Requirements

### 1. Problem Statement
As a Marketing Data Analyst in the healthcare sector, you are tasked with analyzing the return on investment (ROI) for various marketing campaigns. You have collected data regarding the ROI for four different campaigns: Email Marketing, Social Media Advertising, Search Engine Optimization (SEO), and Pay-Per-Click (PPC) advertising. Your objective is to generate a bar chart that visually compares the ROI of these campaigns using the Seaborn library. This exercise will help you apply the concepts learned in the lecture regarding data visualization techniques and enhance your ability to present data-driven insights effectively.

### 2. Fill-in-the-Blank Starter Code
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Sample data for ROI across different campaigns
data = {
    'Campaign': ['Email Marketing', 'Social Media', 'SEO', 'PPC'],
    'ROI': [1500, 2300, 1800, 2200]  # Example ROI values
}

# Create a DataFrame from the data
df = pd.DataFrame(data)

# Starter code for creating a bar chart
def plot_roi_comparison(dataframe):
    # Create a bar plot using Seaborn
    _________.barplot(x='Campaign', y='ROI', data=_________)
    
    # Set the title and labels
    plt.title('ROI Comparison Across Marketing Campaigns')
    plt.xlabel('Campaign Type')
    plt.ylabel('Return on Investment (ROI)')
    
    # Show the plot
    plt.show()

# Call the function to plot the ROI comparison
plot_roi_comparison(_________)
```

### 3. Hints
- Remember to use the correct function from Seaborn to create a bar plot.
- Ensure you are passing the DataFrame you created as an argument to your plotting function.
- Check that your x-axis corresponds to the campaign names and your y-axis corresponds to the ROI values.
- Use the `plt` module to set titles and labels for clarity.

### 4. Expected Outcome
Upon completing this exercise, you should be able to fill in the blanks correctly, demonstrating an understanding of how to visualize marketing campaign performance using Seaborn. The final solution should:
- Generate a clear bar chart comparing the ROI of different marketing campaigns.
- Adhere to best practices by including comments that explain each step of your code.
- Handle any potential errors gracefully, such as ensuring that the DataFrame is not empty before plotting.

### Integration
This exercise is structured to align with the learning objectives of the module, reinforcing your understanding of data visualization in a practical context relevant to your career goals in healthcare marketing. The clear headings and sections facilitate easy integration into your learning platform, ensuring a seamless educational experience.