# Module Title: Building Interactive Dashboards with Plotly and Dash

## Exercise 1: Create an Interactive Scatter Plot for Consumer Behavior Analysis

### Problem Statement
As a Marketing Data Analyst in a healthcare marketing firm, you have been tasked with analyzing consumer behavior based on a recent marketing campaign. Your goal is to create an interactive scatter plot that visualizes the relationship between the age of potential patients and their likelihood of signing up for healthcare services. The data you have includes the age of individuals and a score representing their interest level in the services offered.

Using the concepts discussed in the lecture, create an interactive scatter plot that allows users to filter by interest level and visualize how age correlates with the likelihood of signing up. This will help your team identify which age groups are most engaged and tailor future marketing efforts accordingly.

### Fill-in-the-Blank Starter Code
```python
import dash
from dash import dcc, html
import plotly.express as px
import pandas as pd

# Sample DataFrame simulating consumer behavior data
data = pd.DataFrame({
    'Age': [25, 30, 35, 40, 45, 50, 55, 60],
    'Interest_Score': [5, 6, 7, 8, 9, 4, 3, 2],
    'Sign_Up_Likelihood': [1, 0, 1, 1, 0, 0, 1, 0]
})

app = dash.Dash(__name__)

app.layout = html.Div(children=[
    html.H1(children='Consumer Behavior Analysis'),
    
    dcc.Graph(
        id='age-interest-scatter',
        figure=px.scatter(data, x='Age', y='Interest_Score',
                          color='Sign_Up_Likelihood',
                          title='Scatter Plot of Age vs. Interest Score')
    ),
    
    # Add a dropdown for filtering by interest score
    dcc.Dropdown(
        id='interest-filter',
        options=[
            {'label': 'High Interest (7-10)', 'value': 'High'},
            {'label': 'Low Interest (0-6)', 'value': 'Low'}
        ],
        value='High',  # Default value
        multi=False
    )
])

if __name__ == '__main__':
    app.run_server(debug=True)
```

### Hints
1. **Understanding the Data**: Think about how age might impact a consumer's interest in healthcare services. What trends do you expect to see?
2. **Interactive Elements**: Consider how you can use Dash components to allow users to filter or interact with the data. What components would best serve this purpose?
3. **Plotly Express**: Remember that Plotly Express makes it easy to create scatter plots. Review how you can use it to map your data points effectively.
4. **Data Filtering**: You will need to implement a callback function to update the scatter plot based on the selected interest score from the dropdown.

### Expected Outcome
Upon completing this exercise, you should be able to:
- Fill in the blanks correctly to create an interactive scatter plot that visualizes consumer behavior trends.
- Demonstrate an understanding of how to use Dash and Plotly Express to create dynamic visualizations.
- Implement interactivity that allows stakeholders to filter data based on interest levels.
- Provide well-commented code that explains each step of your implementation.

This exercise aligns with your career goals as a Marketing Data Analyst and will help you build a portfolio of data visualization projects that showcase your skills in analyzing consumer behavior trends in healthcare marketing.