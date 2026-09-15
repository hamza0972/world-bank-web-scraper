# World Bank Country Data Web Scraper

A Python web scraper that extracts country-level economic and demographic data from the [World Bank](https://data.worldbank.org/) website using Requests and BeautifulSoup.

The scraper automatically collects data from individual country pages, handles multiple country URLs, extracts selected indicators, and stores the results in a structured CSV file.

---

## 📌 Project Overview

This project was created as a hands-on practice project to learn and apply Python web scraping techniques.

The scraper first collects the links of individual countries from the World Bank country directory. It then visits each country page and extracts selected economic and demographic indicators.

The collected information is finally stored in a CSV file for further analysis and processing.

---

## 🚀 Features

- Extracts country links from the World Bank website
- Scrapes data from multiple country pages
- Extracts country names
- Extracts life expectancy data
- Extracts poverty information
- Extracts population data
- Extracts population growth data
- Extracts net migration data
- Extracts GDP data
- Handles unavailable data
- Checks HTTP response status
- Uses URL joining for complete country URLs
- Stores structured data in CSV format
- Can be run using Jupyter Notebook or Google Colab

---

## 🛠️ Technologies Used

- **Python**
- **Requests**
- **BeautifulSoup**
- **CSV**
- **Jupyter Notebook**
- **Google Colab**
- **HTML Parsing**

---

## 📊 Data Extracted

The scraper collects the following information for each country:

| Field | Description |
|---|---|
| Country | Name of the country |
| Life Expectancy | Life expectancy at birth |
| Poverty | Poverty-related indicator |
| Population | Total population |
| Population Growth | Annual population growth |
| Net Migration | Net migration indicator |
| GDP | Gross Domestic Product |

---

## 🔄 How It Works

The scraper follows a two-stage process.

### Stage 1: Collect Country Links

The scraper starts from the World Bank country directory and:

1. Sends an HTTP request to the country directory.
2. Parses the HTML using BeautifulSoup.
3. Finds the country sections.
4. Extracts country links.
5. Combines relative URLs with the World Bank base URL.
6. Stores all country URLs in a list.

### Stage 2: Extract Country Data

For every country URL:

1. Sends an HTTP request.
2. Checks whether the request was successful.
3. Parses the webpage HTML.
4. Finds the indicator sections.
5. Extracts the country name.
6. Extracts life expectancy.
7. Extracts poverty information.
8. Extracts population.
9. Extracts population growth.
10. Extracts net migration.
11. Extracts GDP.
12. Stores the extracted information in lists.

Finally, all lists are combined and written to a CSV file.

---

## 🧩 Scraping Workflow

```text
World Bank Country Directory
          ↓
    Send HTTP Request
          ↓
      Parse HTML
          ↓
   Find Country Links
          ↓
     Store URLs
          ↓
 Visit Each Country Page
          ↓
    Parse Country HTML
          ↓
 Extract Selected Indicators
          ↓
 Handle Missing Data
          ↓
      Store Results
          ↓
       CSV File
