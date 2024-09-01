### Lecture: Basic Data Types and Structures in Python

#### 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Identify and define basic data types in Python, including integers, floats, strings, and booleans.
- Understand and utilize core data structures such as lists, tuples, dictionaries, and sets.
- Apply these data types and structures in simple Python scripts relevant to marketing data analysis.

#### 2. Introduction:
In this lecture, we will explore the fundamental building blocks of Python: its basic data types and structures. Understanding these concepts is crucial for a Marketing Data Analyst as they form the foundation for data manipulation and analysis. By effectively using these data types and structures, you can analyze consumer behavior trends, automate marketing performance reports, and build interactive dashboards that provide insights into marketing campaigns. This knowledge will empower you to make data-driven decisions that enhance your marketing strategies.

#### 3. Core Concepts:
- **Basic Data Types**:
  - **Integers**: Whole numbers used for counting (e.g., number of sales).
  - **Floats**: Decimal numbers used for precise values (e.g., revenue).
  - **Strings**: Text data (e.g., customer names, product descriptions).
  - **Booleans**: True/False values used for conditional statements (e.g., whether a campaign was successful).

- **Core Data Structures**:
  - **Lists**: Ordered collections of items that can be changed (mutable). Example: `sales_data = [100, 200, 300]`.
  - **Tuples**: Ordered collections that cannot be changed (immutable). Example: `campaign_info = ("Campaign A", 2023)`.
  - **Dictionaries**: Key-value pairs that allow for efficient data retrieval. Example: `marketing_metrics = {"ROI": 150, "CTR": 0.05}`.
  - **Sets**: Unordered collections of unique items. Example: `unique_customers = {"John", "Jane", "Doe"}`.

#### 4. Practical Application:
Consider a scenario where you want to analyze the performance of various marketing campaigns. You might collect data on each campaign's ROI and click-through rates (CTR) using a dictionary:

```python
# Sample dictionary to store marketing metrics
marketing_metrics = {
    "Campaign A": {"ROI": 150, "CTR": 0.05},
    "Campaign B": {"ROI": 200, "CTR": 0.07}
}

# Accessing data
for campaign, metrics in marketing_metrics.items():
    print(f"{campaign} - ROI: {metrics['ROI']}, CTR: {metrics['CTR']}")
```

This simple example demonstrates how to organize and access campaign data effectively, enabling you to visualize trends in consumer behavior.

#### 5. Summary:
In this lecture, we covered the basic data types (integers, floats, strings, booleans) and core data structures (lists, tuples, dictionaries, sets) in Python. These concepts are essential for any aspiring Marketing Data Analyst as they facilitate the organization and manipulation of data necessary for insightful analysis. Remember that mastering these basics will significantly enhance your ability to analyze marketing performance and consumer behavior.

#### 6. Next Steps:
In the next lecture, we will delve into control flow in Python, including conditional statements and loops. This will allow you to automate processes and make your analyses more dynamic. To prepare, review the basic concepts discussed today and think about how you might use these data types and structures in your own marketing analytics projects.