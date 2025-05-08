Absolutely, here’s a detailed and polished `README.md` file for your project. You can copy this as-is into a `README.md` file or tweak it further if needed.

---

## 📰 News Aggregator with API, Web Scraping & GUI

### 📌 Overview

This project is a **News Aggregator application** that fetches top headlines from a public news API, enriches them with additional details via **web scraping**, and presents them in a **popup GUI** built with **Tkinter**. It also includes **visualization** and **unit testing**, making it a complete, interactive Python application.

---

### ✨ Key Features

* ✅ Fetches latest news articles from [NewsAPI.org](https://newsapi.org)
* ✅ Scrapes full article content, author, and publish date using `BeautifulSoup`
* ✅ Caches responses locally to minimize API calls
* ✅ Cleans and processes data using `pandas`
* ✅ Displays data in a scrollable, sortable **Tkinter TreeView GUI**
* ✅ Double-click any article to open the source in your browser
* ✅ Visualizes:

  * 📊 Article count by source
  * 📈 Article publication trend over time
* ✅ Includes unit tests using `unittest`

---

### 📁 Project Structure

| File                    | Purpose                                         |
| ----------------------- | ----------------------------------------------- |
| `main.py` (your script) | Main application with GUI, API, scraping, tests |
| `news_cache.json`       | Cache file to store fetched articles            |
| `README.md`             | This documentation file                         |

---

### 🧠 How It Works

1. **NewsFetcher**
   Calls the NewsAPI to retrieve metadata (title, source, author, publish date, URL).

2. **WebScraper**
   Uses `requests` and `BeautifulSoup` to extract full content, author, and published date if missing from the API.

3. **NewsAggregator**
   Combines and cleans this data, removing duplicates and filling missing values. Also supports caching.

4. **GUI (Tkinter)**
   Displays the articles in a table (Treeview) with columns: Title, Author, Source, Published At, and URL.

   * Double-clicking a row opens the article in your browser.

5. **Visualization (Matplotlib)**

   * Bar chart: articles per source
   * Line chart: articles over time (parsed from publish dates)

6. **Unit Testing**
   Validates core functionality such as article creation, scraping, and data cleaning.

---

### 🚀 How to Run

#### 🛠 Requirements

Install required Python packages:

```bash
pip install requests beautifulsoup4 pandas matplotlib
```

#### ▶️ Running the App

From your terminal or Python environment:

```bash
python main.py
```

> 🔹 This will launch a Tkinter window with category and article selection, buttons to fetch or visualize data.

#### 🧪 Running Unit Tests

Unit tests will automatically run at the bottom of the script (or you can isolate them):

```bash
python main.py
```

Or to isolate test execution:

```bash
python -m unittest main.py
```

---

### 📌 Notes

* You need a valid API key from [https://newsapi.org](https://newsapi.org).

  * Replace `API_KEY` in the script with your own key.
* Be mindful of API rate limits.
* Ethical scraping practices are followed: only public metadata is scraped.

---

### 💡 Future Ideas

* Add "Save to CSV" or "Export to Excel" button
* Add date filtering or source selection
* Convert to web app using Flask or Streamlit

---

Let me know if you'd like me to generate the README as a downloadable `.md` file too!
