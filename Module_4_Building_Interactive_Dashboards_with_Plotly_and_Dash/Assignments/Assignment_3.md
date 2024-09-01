### Assignment: Deploy Your Dashboard on a Cloud Platform

#### Problem Statement
As a Marketing Data Analyst in the Healthcare Marketing sector, you are tasked with creating a dashboard that visualizes key marketing performance metrics. Your goal is to deploy this dashboard on a cloud platform so that stakeholders can access real-time data regarding marketing performance. This assignment will help you apply the skills learned in the lecture on creating interactive visualizations with Plotly and prepare you for real-world applications in marketing analytics.

#### Starter Code
Below is a basic framework to get you started on your dashboard using Plotly and Dash. You will need to build upon this code to create a fully functional dashboard that can be deployed.

```python
import dash
from dash import dcc, html
import plotly.graph_objects as go

# Sample data for demonstration purposes
months = ['January', 'February', 'March', 'April']
sales = [15000, 20000, 25000, 30000]

# Initialize the Dash app
app = dash.Dash(__name__)

# Define the layout of the app
app.layout = html.Div([
    html.H1("Marketing Performance Dashboard"),
    dcc.Graph(
        id='sales-line-chart',
        figure={
            'data': [
                go.Scatter(x=months, y=sales, mode='lines+markers', name='Sales')
            ],
            'layout': go.Layout(
                title='Monthly Sales Trend',
                xaxis_title='Month',
                yaxis_title='Sales ($)',
                hovermode='x unified'
            )
        }
    ),
    html.Div(id='output-container')
])

# Run the app
if __name__ == '__main__':
    app.run_server(debug=True)
```

#### Detailed Instructions
1. **Modify the Sample Data**:
   - Replace the `months` and `sales` lists with actual marketing performance data relevant to your organization. You can simulate this data or use any dataset you have access to.

2. **Add Interactivity**:
   - Enhance your dashboard by adding dropdowns or sliders to allow users to filter the data dynamically. For example, you could let users select a specific region or product category to view corresponding sales data.
   - Use `dcc.Dropdown` or `dcc.Slider` components from Dash for this purpose.

3. **Deploying on a Cloud Platform**:
   - Once your dashboard is complete and running locally, you will need to deploy it on a cloud platform such as Heroku or AWS.
   - Follow the platform-specific instructions for deployment. For Heroku, you may need to create a `requirements.txt` file that lists all necessary packages (like Dash and Plotly) and a `Procfile` to specify how to run your app.
   - Ensure that your app is accessible via a public URL after deployment.

4. **Testing Your Dashboard**:
   - Test your deployed dashboard to ensure that it displays correctly and that all interactive features work as intended. Share the URL with peers for feedback.

#### Criteria for Success and Evaluation
- **Functionality**: The dashboard must display accurate marketing performance data and allow users to interact with it effectively.
- **Code Quality**: Your code should be clean, well-organized, and include comments explaining the purpose of each section.
- **Deployment**: Successfully deploy your dashboard on a cloud platform, ensuring it is accessible via a public URL.
- **User Experience**: The dashboard should be user-friendly, with clear labels and intuitive navigation.

By completing this assignment, you will not only reinforce your understanding of creating interactive visualizations using Plotly but also gain practical experience in deploying web applications—skills that are essential for your career as a Marketing Data Analyst in the healthcare industry.