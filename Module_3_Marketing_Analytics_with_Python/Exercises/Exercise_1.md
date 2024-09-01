### Module Title: Marketing Analytics with Python

### Exercise Requirements 

#### 1. Problem Statement
As a Marketing Data Analyst in the healthcare industry, you are tasked with understanding consumer behavior trends by analyzing data from a healthcare marketing website. Your goal is to scrape relevant data, such as the number of visits to different service pages (e.g., cardiology, oncology, pediatrics) and the demographics of the visitors (age groups). This data will help you tailor marketing strategies to improve patient engagement and health outcomes.

Using BeautifulSoup, write a Python script to scrape this data from the provided marketing website. After scraping, visualize the data to identify which service pages attract the most visitors from different age groups.

#### 2. Fill-in-the-Blank Starter Code
```python
import requests
from bs4 import BeautifulSoup
import pandas as pd
import matplotlib.pyplot as plt

# Step 1: Send a request to the website
url = 'http://example-healthcare-marketing-website.com'  # Replace with the actual URL
response = requests.get(url)

# Step 2: Parse the content of the page
soup = BeautifulSoup(response.content, 'html.parser')

# Step 3: Find the relevant data on the page
# Assume we are looking for a table with service pages and visit counts
data = []
table = soup.find('table', {'id': 'service-visits'})  # Adjust based on actual HTML structure
rows = table.find_all('tr')

for row in rows[1:]:  # Skip header row
    columns = row.find_all('td')
    service_page = columns[0].text.strip()  # Service name
    visits = int(columns[1].text.strip())  # Number of visits
    age_group = columns[2].text.strip()  # Age group
    data.append({'Service Page': service_page, 'Visits': visits, 'Age Group': age_group})

# Step 4: Create a DataFrame from the scraped data
df = pd.DataFrame(data)

# Step 5: Visualize the data
# Fill in the blanks below to create a bar chart of visits by service page
plt.figure(figsize=(10, 6))
plt.bar(df['Service Page'], df['Visits'], color='skyblue')
plt.title('Visits by Service Page')
plt.xlabel('Service Page')
plt.ylabel('Number of Visits')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
```

#### 3. Hints
- **Hint 1**: When scraping data, ensure you inspect the HTML structure of the webpage to correctly identify the elements containing the information you need.
- **Hint 2**: Use `soup.find()` or `soup.find_all()` methods to locate specific tags or classes in the HTML.
- **Hint 3**: After scraping, remember to convert any numerical values from strings to integers for accurate analysis.
- **Hint 4**: When visualizing data, consider using different colors or styles to differentiate between age groups if you decide to extend your analysis.

#### 4. Expected Outcome
By completing this exercise, you should be able to:
- Successfully scrape data from a healthcare marketing website using BeautifulSoup.
- Create a DataFrame that organizes the scraped data effectively.
- Visualize consumer behavior trends by generating a bar chart that displays visits by service page.
- Demonstrate an understanding of how marketing analytics can inform strategies in healthcare marketing.

This exercise not only reinforces the concepts discussed in the lecture but also provides practical experience relevant to your career goals as a Marketing Data Analyst.