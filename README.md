# AI Web Scraper

Welcome to the AI Web Scraper project! This project is designed to scrape web content, clean it, and parse it using AI techniques. The project leverages Streamlit for the user interface, Selenium for web scraping, and various Python libraries for content processing.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Using ChromeDriver Locally](#using-chromedriver-locally)
- [Credits](#credits)
- [License](#license)

## Introduction

This project was created by Ansh Jain. It provides a simple and efficient way to scrape web content and process it using AI techniques. The project was inspired by a tutorial from Tech With Tim, which made the implementation process easy to understand.

## Features

- Web scraping using Selenium
- Content extraction and cleaning
- Parsing content with AI
- User-friendly interface with Streamlit

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/yourusername/AI-Web-Scraper.git
    cd AI-Web-Scraper
    ```

2. **Create a Virtual Environment**:
    ```sh
    python -m venv venv
    ```

3. **Activate the Virtual Environment**:
    - On Windows:
        ```sh
        .\venv\Scripts\activate
        ```
    - On macOS/Linux:
        ```sh
        source venv/bin/activate
        ```

4. **Install Dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

Follow these steps to run the project:

1. **Run the Streamlit Application**:
    ```sh
    streamlit run main.py
    ```

2. **Open the Application in Your Browser**:
    - The application will automatically open in your default web browser. If it doesn't, navigate to `http://localhost:8501` in your browser.

3. **Enter the Website URL**:
    - Enter the URL of the website you want to scrape in the input field and click the "Scrape Website" button.

4. **View the Results**:
    - The scraped content, cleaned content, and parsed content will be displayed on the web interface.

## Using ChromeDriver Locally

For local development and testing, you can use ChromeDriver instead of Bright Data. ChromeDriver is a standalone server that implements the WebDriver protocol for Chrome. Here are the steps to set it up:

1. **Download ChromeDriver**:
    - Download the ChromeDriver executable from the [official site](https://sites.google.com/a/chromium.org/chromedriver/downloads) and place it in a directory of your choice.

2. **Update [scrape.py](http://_vscodecontentref_/1)**:
    - Modify the `scrape_website` function to use ChromeDriver locally:
    ```python
    from selenium import webdriver
    from selenium.webdriver.chrome.service import Service as ChromeService
    from selenium.webdriver.chrome.options import Options

    def scrape_website(url):
        chrome_service = ChromeService(executable_path='path/to/chromedriver')
        chrome_options = Options()
        driver = webdriver.Chrome(service=chrome_service, options=chrome_options)
        driver.get(url)
        html = driver.page_source
        driver.quit()
        return html
    ```

    Replace `'path/to/chromedriver'` with the actual path to your ChromeDriver executable.

## Credits

This project was created by Ansh Jain. Special thanks to [Tech With Tim](https://www.youtube.com/watch?v=Oo8-nEuDBkk&ab_channel=TechWithTim) for the tutorial that made this implementation easy to understand.

Connect with me on [LinkedIn](https://linkedin.com/in/ansh--jain).

## License

This project is licensed under the MIT License. See the LICENSE file for details.


