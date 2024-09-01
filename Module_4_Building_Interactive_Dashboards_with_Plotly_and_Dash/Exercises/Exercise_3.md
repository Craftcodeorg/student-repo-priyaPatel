### Module Title: Building Interactive Dashboards with Plotly and Dash

### Exercise Requirements

#### 1. Problem Statement
You are tasked with creating an interactive dashboard for a healthcare marketing campaign. The goal is to visualize consumer engagement data over the past year, allowing stakeholders to filter the data by month and type of campaign. This will help in analyzing which marketing strategies were most effective in engaging consumers.

Your dashboard should include:
- A line chart displaying monthly engagement rates.
- Dropdown controls to select different types of campaigns (e.g., Email, Social Media, Direct Mail).
- A slider to filter the data by month.

Implement the interactivity using user input controls as discussed in the lecture. 

#### 2. Fill-in-the-Blank Starter Code
```python
import plotly.graph_objects as go
from plotly.subplots import make_subplots
import pandas as pd

# Sample data for the dashboard
data = {
    'Month': ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
    'Email': [100, 150, 200, 250, 300, 350, 400, 450, 500, 550, 600, 650],
    'Social Media': [80, 120, 160, 200, 240, 280, 320, 360, 400, 440, 480, 520],
    'Direct Mail': [60, 90, 120, 150, 180, 210, 240, 270, 300, 330, 360, 390]
}

# Convert data into a DataFrame
df = pd.DataFrame(data)

# Create a function to update the chart based on user input
def update_chart(selected_campaign):
    # Filter data based on the selected campaign
    filtered_data = df[['Month', selected_campaign]]
    
    # Create a line chart
    fig = go.Figure()
    fig.add_trace(go.Scatter(x=filtered_data['Month'], 
                              y=filtered_data[selected_campaign], 
                              mode='lines+markers', 
                              name=selected_campaign))
    
    # Update layout
    fig.update_layout(title='Monthly Engagement Rates by Campaign',
                      xaxis_title='Month',
                      yaxis_title='Engagement Rate',
                      hovermode='x unified')
    
    # Show the figure
    fig.show()

# Dropdown options for campaign types
campaign_types = ['Email', 'Social Media', 'Direct Mail']

# Call the update_chart function with a default campaign type
update_chart(_____)  # Fill in with a default campaign type (e.g., 'Email')
```

#### 3. Hints
- To implement the dropdown functionality, you will need to use Plotly's `dcc.Dropdown` component from the Dash library.
- Remember to use the `update_chart` function to dynamically update the chart based on user selections.
- Think about how you can use callbacks in Dash to link user input controls with your visualizations.

#### 4. Expected Outcome
By completing this exercise:
- You should be able to fill in the blanks correctly to implement a functional interactive dashboard.
- Your final code should demonstrate an understanding of how to create interactive visualizations using Plotly and Dash.
- The code should be well-commented to explain each step and include error handling where necessary.

### Integration
This exercise is designed to reinforce the concepts covered in the lecture on creating interactive visualizations with Plotly. It aligns with your interests in data visualization and marketing analytics while providing a practical application relevant to your career goals in healthcare marketing.