# Walmart Web Scraper

## Overview

This Python script performs web scraping on a Walmart product page to extract and monitor the price of a specific item. It utilizes the BeautifulSoup library for HTML parsing and requests library for making HTTP requests. The extracted data is then stored in a CSV file, and the script can be scheduled to run at regular intervals to keep track of price changes.

## Prerequisites

- Python 3.x
- Libraries: BeautifulSoup, requests, smtplib, time, datetime, csv
- Gmail account for email notifications (optional)

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/your-username/Walmart-Web-Scraper.git
cd Walmart-Web-Scraper
```

2. Install the required libraries:

```bash
pip install -r requirements.txt
```

3. Update the script with your Gmail credentials if you want to enable email notifications:

```python
# Update these lines in the script
server.login('your-email@gmail.com', 'your-email-password')
```

4. Run the script:

```bash
python walmart_scraper.py
```

## Script Details

- **`check_price()`**: Function to scrape the Walmart product page, extract title and price, and append the data to the CSV file.

- **`send_mail()`**: Function to send an email notification when the price drops below a certain level (optional, requires Gmail credentials).

- **`while(True)` loop**: Runs the `check_price()` function at regular intervals (every 24 hours in this example).

## CSV Output

The scraped data is stored in a CSV file named `WalmartWebScraperDataset.csv` with columns: 'Title', 'Price', and 'Date'.

## Notes

- The script can be modified to track prices for different products by updating the `URL` variable.
- Adjust the sleep interval in the `time.sleep()` function to control how frequently the script checks the price.
