### Module Title: Marketing Analytics with Python

### Exercise Requirements

1. **Problem Statement**:
   You are tasked with analyzing the performance of a recent marketing campaign for a new healthcare product. The campaign involved various online platforms, and you have collected data from consumer reviews, social media mentions, and competitor pricing. Your goal is to scrape relevant data from a review website and visualize the insights to evaluate the campaign's effectiveness.

   Using the concepts learned in the lecture on web scraping, complete the following tasks:
   - Scrape consumer reviews from a designated website.
   - Analyze the sentiment of these reviews.
   - Create a simple visualization to showcase the findings regarding consumer sentiment towards the healthcare product.

2. **Fill-in-the-Blank Starter Code**:
   Below is a starter code snippet that you will need to complete. Fill in the blanks to implement the web scraping functionality and analyze the data.

   ```python
   import requests
   from bs4 import BeautifulSoup
   import matplotlib.pyplot as plt
   from collections import Counter

   # Function to scrape reviews from a webpage
   def scrape_reviews(url):
       # Step 1: Send a request to the webpage
       response = requests.get(url)
       # Step 2: Parse the content
       soup = BeautifulSoup(response.content, 'html.parser')
       # Step 3: Extract data (e.g., review texts)
       reviews = soup.find_all('div', class_='review-text')
       review_list = [review.text for review in reviews]
       return review_list

   # Function to analyze sentiment (dummy implementation)
   def analyze_sentiment(reviews):
       # Simple sentiment analysis based on keywords
       positive_keywords = ['good', 'great', 'excellent', 'love']
       negative_keywords = ['bad', 'poor', 'hate', 'worst']
       
       sentiments = []
       for review in reviews:
           if any(word in review.lower() for word in positive_keywords):
               sentiments.append('Positive')
           elif any(word in review.lower() for word in negative_keywords):
               sentiments.append('Negative')
           else:
               sentiments.append('Neutral')
       
       return sentiments

   # Function to visualize sentiment distribution
   def visualize_sentiment(sentiments):
       sentiment_count = Counter(sentiments)
       labels = sentiment_count.keys()
       sizes = sentiment_count.values()

       # Create a pie chart
       plt.figure(figsize=(8, 8))
       plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=140)
       plt.title('Sentiment Analysis of Consumer Reviews')
       plt.axis('equal')  # Equal aspect ratio ensures that pie chart is circular.
       plt.show()

   # Main execution
   url = 'https://www.example.com/reviews'  # Replace with actual URL
   reviews = scrape_reviews(url)  # Scrape reviews
   sentiments = analyze_sentiment(reviews)  # Analyze sentiment
   visualize_sentiment(sentiments)  # Visualize results
   ```

3. **Hints**:
   - For scraping, ensure you are correctly identifying the HTML elements that contain the review text. Use the browser's inspect tool to find the appropriate class or tag.
   - When analyzing sentiment, think about how you can categorize reviews based on specific keywords. You can expand the list of keywords as needed.
   - For visualization, remember that `matplotlib` allows you to create various types of plots. A pie chart is a good choice for displaying sentiment distribution.

4. **Expected Outcome**:
   By completing this exercise, you should be able to successfully scrape consumer reviews from a webpage, analyze their sentiment, and visualize the results in a clear and informative way. Your final code should demonstrate an understanding of web scraping techniques, basic sentiment analysis, and data visualization best practices. Comments in your code should explain your thought process and the purpose of each function.

### Integration
- Ensure that all code snippets are properly formatted using markdown for clarity.
- Include links to additional resources on web scraping ethics and best practices if necessary.
- Structure the exercise with clear headings and sections to facilitate easy navigation and understanding.