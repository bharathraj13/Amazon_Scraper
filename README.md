**Project Title: Amazon Product Scraper**

**Description**

This project is a web scraper designed to extract product information from Amazon's search results. It retrieves details such as product titles, prices, ratings, number of user reviews, and availability status for products listed under a specific search query. The extracted data is then saved into a CSV file for further analysis.

**Features**

Extracts product title, price, rating, review count, and availability status.
Handles potential missing data gracefully.
Saves the collected data into a CSV file named amazon_data.csv.

**Technologies Used**

Python: Programming language used for the implementation.
BeautifulSoup: Library for parsing HTML and XML documents.
Requests: Library for making HTTP requests to fetch web pages.
Pandas: Library for data manipulation and analysis.
NumPy: Library for numerical operations (used here for handling NaN values).

**Installation**

1. Ensure you have Python installed on your machine. You can download it from python.org.
2. Install the required libraries using pip:

  pip install beautifulsoup4 requests pandas numpy

**Usage**

Open the script in your preferred Python environment or IDE.

Modify the URL variable if you want to search for different products on Amazon.

Run the script:

python amazon_scraper.py

After execution, check the directory for the amazon_data.csv file containing the scraped product data.

**Functions Overview**

get_title(soup): Extracts the product title from the HTML soup.
get_price(soup): Extracts the product price, checking multiple possible price IDs.
get_rating(soup): Extracts the product rating from the HTML soup.
get_review_count(soup): Extracts the number of user reviews from the HTML soup.
get_availability(soup): Extracts the availability status of the product.

**Example Output**

The script will generate a CSV file (amazon_data.csv) with columns:
**title:** The name of the product.

**price:** The price of the product.

**rating:** The rating given by users.

**reviews:** The number of reviews received.

**availability:** Availability status (e.g., "In Stock", "Not Available").

**Important Notes**

1. Web scraping may violate the terms of service of some websites, including Amazon. Ensure you comply with their policies before scraping data.
2. The structure of Amazon's web pages may change over time, which could break this scraper. Adjustments to the scraping logic may be necessary if elements are not found.
