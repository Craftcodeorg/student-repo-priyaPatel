### Module Title: Building Interactive Dashboards with Plotly and Dash ###

### Exercise Requirements ###

1. **Problem Statement**: 
   You are tasked with creating a basic Dash application that visualizes marketing metrics for a healthcare product launch. The goal is to display consumer purchase data dynamically, allowing stakeholders to analyze trends based on different demographics and time periods. You will use the Plotly and Dash libraries to create an interactive dashboard that can filter sales data by region and age group. This exercise will help you apply the concepts learned in the lecture about visualizing consumer behavior trends and automating marketing performance reports.

2. **Fill-in-the-Blank Starter Code**:
   Below is a starter code template for your Dash app. Fill in the blanks where indicated to complete the functionality. 

   ```python
   import plotly.express as px
   import dash
   from dash import dcc, html
   from dash.dependencies import Input, Output

   # Sample data for healthcare product sales
   data = {
       'Region': ['North', 'South', 'East', 'West'],
       'Sales': [15000, 20000, 30000, 25000],
       'Age Group': ['18-25', '26-35', '36-45', '46-55']
   }

   # Create a Plotly figure for sales by region
   fig = px.bar(data, x='Region', y='Sales', title='Sales by Region')

   # Initialize Dash app
   app = dash.Dash(__name__)

   # Layout of the dashboard
   app.layout = html.Div(children=[
       html.H1(children='Healthcare Product Sales Dashboard'),
       
       # Dropdown for selecting age group
       dcc.Dropdown(
           id='age-group-dropdown',
           options=[
               {'label': '18-25', 'value': '18-25'},
               {'label': '26-35', 'value': '26-35'},
               {'label': '36-45', 'value': '36-45'},
               {'label': '46-55', 'value': '46-55'}
           ],
           value='18-25'  # Default value
       ),

       # Graph to display sales data
       dcc.Graph(id='sales-graph', figure=fig)
   ])

   # Callback to update the graph based on selected age group
   @app.callback(
       Output('sales-graph', 'figure'),
       Input('age-group-dropdown', 'value')
   )
   def update_graph(selected_age_group):
       # Filter data based on selected age group (fill in the blank)
       filtered_data = _______  # Filter logic here
       
       # Create a new figure based on filtered data
       new_fig = px.bar(filtered_data, x='Region', y='Sales', title='Sales by Region for Age Group: ' + selected_age_group)
       return new_fig

   if __name__ == '__main__':
       app.run_server(debug=True)
   ```

3. **Hints**:
   - To filter the data based on the selected age group, consider using a conditional statement that checks the `Age Group` key in your dataset.
   - Remember that you can use Pandas to handle data filtering if you convert your data into a DataFrame.
   - Make sure your graph updates dynamically when a different age group is selected from the dropdown.

4. **Expected Outcome**:
   By completing this exercise, you should be able to fill in the blanks correctly to create a functional Dash app that displays sales metrics for different age groups. The final solution should demonstrate your understanding of how to use Plotly and Dash for real-world marketing analytics in the healthcare industry. Ensure that your code is well-commented to explain each step and includes error handling where necessary.

### Integration ###
- Ensure the exercise content is well-structured, with clear headings and sections for easy parsing and integration into the learning platform. Use markdown for formatting and include any necessary files or resources as links. 

This exercise will provide you with practical experience in building interactive dashboards, aligning with your career goals as a Marketing Data Analyst in Healthcare Marketing.