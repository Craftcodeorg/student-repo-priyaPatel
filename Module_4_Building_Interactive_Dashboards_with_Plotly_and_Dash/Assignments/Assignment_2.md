### Assignment: Create a Data Filtering Application with Dash

#### Problem Statement:
As a Marketing Data Analyst in the healthcare sector, you are tasked with creating a web application that allows users to filter marketing campaign data by campaign type. This application will help stakeholders visualize the effectiveness of different campaigns and make informed decisions based on consumer behavior trends. Using the concepts learned in the lecture on Plotly and Dash, you will build an interactive dashboard that displays relevant metrics and enables filtering by campaign type.

#### Starter Code:
Below is a basic framework for your Dash application. This starter code sets up the environment and includes comments to guide you on where to implement your solutions.

```python
import dash
from dash import dcc, html, Input, Output
import plotly.express as px
import pandas as pd

# Sample data: Replace this with your actual campaign data
data = {
    'Campaign Type': ['Email', 'Social Media', 'SEO', 'Email', 'Social Media'],
    'Clicks': [150, 200, 300, 250, 400],
    'Conversions': [30, 50, 70, 40, 90]
}

# Create a DataFrame
df = pd.DataFrame(data)

# Initialize Dash app
app = dash.Dash(__name__)

# Layout of the dashboard
app.layout = html.Div(children=[
    html.H1(children='Marketing Campaign Dashboard'),
    
    # Dropdown for selecting campaign type
    dcc.Dropdown(
        id='campaign-type-dropdown',
        options=[{'label': campaign, 'value': campaign} for campaign in df['Campaign Type'].unique()],
        value='Email'  # Default value
    ),
    
    # Graph for displaying filtered data
    dcc.Graph(id='campaign-graph')
])

# Callback to update graph based on selected campaign type
@app.callback(
    Output('campaign-graph', 'figure'),
    Input('campaign-type-dropdown', 'value')
)
def update_graph(selected_campaign):
    filtered_df = df[df['Campaign Type'] == selected_campaign]
    
    # Create a bar chart for the filtered data
    fig = px.bar(filtered_df, x='Campaign Type', y='Clicks', title=f'Clicks for {selected_campaign} Campaign')
    
    return fig

if __name__ == '__main__':
    app.run_server(debug=True)
```

#### Detailed Instructions:
1. **Set Up Your Environment**:
   - Ensure you have the necessary libraries installed. You can install them using pip:
     ```bash
     pip install dash plotly pandas
     ```

2. **Modify the Sample Data**:
   - Replace the sample data in the `data` dictionary with your actual marketing campaign data. Ensure that your data includes at least the columns for 'Campaign Type', 'Clicks', and 'Conversions'.

3. **Enhance the Graph**:
   - Update the `update_graph` function to create a more informative visualization. Consider adding another metric to visualize, such as 'Conversions' alongside 'Clicks'. You can use `plotly.graph_objects` for more complex visualizations if needed.

4. **Add More Interactivity**:
   - Implement additional filters or controls (e.g., date range picker) to allow users to filter campaigns based on other dimensions like time or performance metrics.

5. **Test Your Application**:
   - Run your Dash application and test it by selecting different campaign types from the dropdown menu. Ensure that the graph updates correctly based on your selection.

#### Criteria for Success and Evaluation:
- **Functionality**: The application should correctly filter and display data based on the selected campaign type.
- **Code Quality**: Your code should be clean, well-documented, and follow best practices (e.g., meaningful variable names, modular functions).
- **User Experience**: The dashboard should be user-friendly, with clear labels and titles that enhance understanding.
- **Visual Appeal**: The graphs should be visually appealing and effectively communicate the data insights.

This assignment will help you apply the concepts from the lecture in a practical setting while reinforcing your skills in data visualization relevant to healthcare marketing analytics. Good luck!