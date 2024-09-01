### Assignment: Visualize Consumer Behavior Trends Using a Line Chart

#### Problem Statement
As a Marketing Data Analyst in the healthcare marketing sector, understanding consumer behavior trends is essential for crafting effective marketing strategies. Your task is to visualize consumer behavior trends over a six-month period using a line chart. You will annotate key events that might have influenced consumer behavior during this time, such as product launches or marketing campaigns. This exercise will help you apply the concepts of data visualization learned in the lecture and demonstrate your ability to create insightful visual narratives.

#### Starter Code
Below is a basic code framework using Matplotlib. You will need to complete the code by adding your own data and annotations based on hypothetical consumer behavior trends.

```python
import matplotlib.pyplot as plt

# Sample data: Monthly consumer engagement scores (hypothetical)
months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
engagement_scores = [70, 80, 90, 85, 95, 100]  # Example engagement scores

# Creating the line graph
plt.figure(figsize=(10, 5))
plt.plot(months, engagement_scores, marker='o', color='blue')
plt.title('Consumer Engagement Trends Over Six Months')
plt.xlabel('Months')
plt.ylabel('Engagement Score')
plt.grid(True)

# Step 1: Annotate key events (you will need to add your own events)
# Example: plt.annotate('Product Launch', xy=('Mar', 90), xytext=('Apr', 92),
#             arrowprops=dict(facecolor='black', shrink=0.05))

# Show the plot
plt.show()
```

#### Detailed Instructions
1. **Modify the Data**: Replace the `engagement_scores` list with your own hypothetical data reflecting consumer engagement scores over six months. Ensure that the data represents realistic trends.

2. **Annotate Key Events**: Identify at least two key events that could have influenced consumer behavior during this period (e.g., product launches, marketing campaigns). Use the `plt.annotate()` function to add annotations to your graph. For example:
   - `plt.annotate('Product Launch', xy=('Mar', 90), xytext=('Apr', 92), arrowprops=dict(facecolor='black', shrink=0.05))`
   - Make sure to adjust the `xy` and `xytext` parameters according to where you want the annotation to appear on the graph.

3. **Enhance Visualization**: Add additional visual elements such as:
   - A legend if you decide to include multiple lines (e.g., comparing different products).
   - Change colors or markers to make your visualization more appealing.

4. **Final Touches**: Ensure that your graph is clear and easy to interpret. Check for spelling errors in your titles and labels.

#### Criteria for Success and Evaluation
Your assignment will be assessed based on the following criteria:

- **Correctness**: The line chart accurately represents the consumer engagement data.
- **Annotations**: At least two key events are correctly annotated with appropriate descriptions.
- **Clarity**: The visualization is clear, well-labeled, and easy to understand.
- **Code Quality**: The code is well-organized and includes comments explaining each part of the process.
- **Creativity**: Efforts to enhance the visualization through color and additional elements will be positively noted.

By completing this assignment, you will gain practical experience in data visualization that is directly applicable to your career goals in healthcare marketing analytics. Good luck!