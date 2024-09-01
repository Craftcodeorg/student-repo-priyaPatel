# Assignment: Build an Interactive Dashboard to Visualize Key Marketing Metrics Over Time

## Problem Statement
As a Marketing Data Analyst in the healthcare industry, your task is to create an interactive dashboard that visualizes key marketing metrics over time. This dashboard will help stakeholders understand the effectiveness of marketing campaigns aimed at increasing patient sign-ups. You will utilize the concepts discussed in the lecture on interactive dashboards to enhance data visualization and facilitate data-driven decision-making.

### Key Metrics to Visualize:
1. Number of patient sign-ups over time.
2. Demographic breakdown of new patients (age, gender).
3. Comparison of campaign performance across different channels (e.g., social media, email).

## Starter Code
Below is the starter code for setting up your interactive dashboard using Plotly and Dash. This code includes a basic structure and some sample data for you to build upon.

```python
import dash
from dash import dcc, html
import plotly.express as px
import pandas as pd

# Sample DataFrame with marketing metrics
data = pd.DataFrame({
    'Date': pd.date_range(start='2023-01-01', periods=12, freq='M'),
    'Sign-ups': [50, 75, 100, 120, 90, 110, 130, 150, 170, 200, 220, 250],
    'Channel': ['Social Media', 'Email', 'Direct Mail', 'Social Media', 'Email',
                'Direct Mail', 'Social Media', 'Email', 'Direct Mail', 'Social Media',
                'Email', 'Direct Mail']
})

# Initialize the Dash app
app = dash.Dash(__name__)

# Layout of the dashboard
app.layout = html.Div(children=[
    html.H1(children='Healthcare Marketing Campaign Performance'),
    
    dcc.Graph(
        id='sign-ups-line-chart',
        figure=px.line(data, x='Date', y='Sign-ups', title='Patient Sign-ups Over Time')
    ),
    
    dcc.Graph(
        id='channel-bar-chart',
        figure=px.bar(data, x='Channel', y='Sign-ups', title='Sign-ups by Marketing Channel')
    )
])

if __name__ == '__main__':
    app.run_server(debug=True)
```

### Instructions
1. **Step 1**: Enhance the line chart to include a dropdown menu that allows users to filter the data by marketing channel (e.g., Social Media, Email, Direct Mail). You will need to modify the layout and add a `dcc.Dropdown` component.
   
2. **Step 2**: Add a pie chart that visualizes the demographic breakdown of new patients based on age and gender. Create a new DataFrame that includes this demographic data and use `plotly.express.pie` to create the chart.

3. **Step 3**: Implement interactivity by allowing users to hover over the charts to see more detailed information about each data point (e.g., exact number of sign-ups on specific dates).

4. **Step 4**: Clean up your code by adding comments explaining what each section does. Ensure that your code is well-structured and follows best practices.

## Criteria for Success and Evaluation
Your assignment will be evaluated based on the following criteria:
- **Functionality**: The dashboard should correctly display the line chart, bar chart, and pie chart with the required interactivity.
- **Code Quality**: The code should be clean, well-organized, and well-documented with comments explaining each part.
- **User Experience**: The dashboard should be user-friendly, allowing easy navigation and exploration of the data.
- **Visual Appeal**: The visualizations should be clear and effectively communicate the marketing metrics.

By completing this assignment, you will gain hands-on experience in building interactive dashboards that are crucial for data visualization in marketing analytics, specifically tailored for your career goal of becoming a Marketing Data Analyst in the healthcare industry.