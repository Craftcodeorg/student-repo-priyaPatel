### Assignment Title: Analyzing Marketing Strategy Effectiveness through Web Scraping

---

### Problem Statement:
As a Marketing Data Analyst in the Healthcare Marketing industry, your task is to analyze consumer sentiment regarding a new healthcare product by scraping reviews from a competitor's website. You will collect data on consumer feedback and analyze the effectiveness of different marketing strategies based on the sentiment of these reviews. This assignment aims to help you apply the web scraping techniques learned in the lecture to gather and analyze real-world marketing data.

---

### Starter Code:
Below is a basic framework for your assignment. You will expand upon this code to scrape review data and analyze it.

```python
import requests
from bs4 import BeautifulSoup
import pandas as pd

def scrape_reviews(url):
    # Step 1: Send a request to the webpage
    response = requests.get(url)
    
    # Step 2: Parse the content
    soup = BeautifulSoup(response.content, 'html.parser')
    
    # Step 3: Extract data (e.g., review titles and sentiments)
    reviews = soup.find_all('div', class_='review')
    review_data = []
    
    for review in reviews:
        title = review.find('h2', class_='review-title').text
        sentiment = review.find('span', class_='review-sentiment').text  # Assume sentiment is provided
        review_data.append({'title': title, 'sentiment': sentiment})
    
    # Convert to DataFrame for analysis
    df = pd.DataFrame(review_data)
    return df

# Example usage
url = 'https://www.example.com/reviews'  # Replace with actual URL
reviews_df = scrape_reviews(url)
print(reviews_df)
```

### Detailed Instructions:
1. **Modify the `scrape_reviews` function**:
   - Update the `url` variable with a valid competitor's website that contains product reviews.
   - Ensure that you correctly identify the HTML structure of the reviews on the webpage. You may need to adjust the `find_all` and `find` methods to match the actual classes used in the HTML.

2. **Analyze Sentiment**:
   - After scraping the data, you need to analyze the sentiment of the reviews. Create a new function `analyze_sentiment(df)` that:
     - Counts the number of positive, negative, and neutral reviews based on the sentiment column.
     - Returns a summary of this analysis.

3. **Enhance Data Output**:
   - Modify your code to provide a summary output that includes:
     - Total number of reviews scraped.
     - Count of each sentiment type (positive, negative, neutral).
     - A sample of the first five reviews.

4. **Documentation**:
   - Ensure your code is well-documented with comments explaining each step. This will help others understand your thought process and code structure.

---

### Criteria for Success and Evaluation:
- **Functionality**: The code correctly scrapes review data from the specified URL and analyzes sentiment.
- **Accuracy**: The sentiment analysis accurately reflects the data scraped, with correct counts for each sentiment type.
- **Code Quality**: The code is clean, well-organized, and follows best practices (e.g., proper variable naming, use of functions).
- **Documentation**: Code is thoroughly documented with comments explaining each section and its purpose.
- **Output Clarity**: The summary output is clear and easy to understand, effectively communicating the results of your analysis.

---

This assignment provides a practical application of web scraping techniques relevant to your role as a Marketing Data Analyst in Healthcare Marketing. By completing this task, you will enhance your skills in data collection and analysis while building a portfolio project that demonstrates your capabilities in marketing analytics.