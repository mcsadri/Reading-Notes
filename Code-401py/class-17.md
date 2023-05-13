# Web Scraping

## Reading

### [Scrape a Dynamic Website with Python](https://scrapingant.com/blog/scrape-dynamic-website-with-python)

- A dynamic website is a type of website that can update or load content after the initial HTML load.
- Usually, dynamic websites use AJAX to load content dynamically, or even the whole site is based on a Single-Page Application (SPA) technology.
- BeautifulSoup is one of the most popular Python libraries across the Internet for HTML parsing.
  - Almost 80% of web scraping Python tutorials use this library to extract required content from the HTML.
- Four different ways to execute dynamic website's Javascript and provide valid data for an HTML parser:
  - Selenium
    - Selenium is one of the most popular web browser automation tools for Python.
    - It allows communication with different web browsers by using a special connector - a webdriver.
    - Selenium instantiating and scraping flow is the following:
      - define and setup Chrome path variable
      - define and setup Chrome webdriver path variable
      - define browser launch arguments (to use headless mode, proxy, etc.)
      - instantiate a webdriver with defined above options
      - load a webpage via instantiated webdriver
  - Pyppeteer
    - Pyppeteer is an unofficial Python port of Puppeteer JavaScript (headless) Chrome/Chromium browser automation library.
      - It is capable of mainly doing the same as Puppeteer can, but using Python instead of NodeJS.
    - Puppeteer is a high-level API to control headless Chrome
  - Playwright
    - Playwright can be considered as an extended Puppeteer, as it allows using more browser types (Chromium, Firefox, and Webkit) to automate modern web app testing and scraping.
  - Web Scraping API
    - ScrapingAnt web scraping API provides an ability to scrape dynamic websites with only a single API call.
      - It already handles headless Chrome and rotating proxies, so the response provided will already consist of Javascript rendered content.
      - ScrapingAnt's proxy poll prevents blocking and provides a constant and high data extraction success rate.
    - You do not need to maintain the browser, library, proxies, webdrivers, or every other aspect of web scraper and focus on the most exciting part of the work - data analysis.
    - To get an API token, please, visit [Login page](https://app.scrapingant.com/login) to authorize in [ScrapingAnt User panel](https://app.scrapingant.com/dashboard). It's free.

### [What is Web Scraping?](https://en.wikipedia.org/wiki/Web_scraping)

- It is a form of copying in which specific data is gathered and copied from the web, typically into a central local database or spreadsheet, for later retrieval or analysis.
- Scraping a web page involves fetching it and extracting from it.
  - Fetching is the downloading of a page (which a browser does when a user views a page).
  - Therefore, web crawling is a main component of web scraping, to fetch pages for later processing. Once fetched, extraction can take place.
  - The content of a page may be parsed, searched and reformatted, and its data copied into a spreadsheet or loaded into a database.
  - Web scrapers typically take something out of a page, to make use of it for another purpose somewhere else.
- As well as contact scraping, web scraping is used as a component of applications used for web indexing, web mining and data mining, etc.
- Techniques:
  - Human copy-and-paste
  - Text pattern matching
  - HTTP programming
  - HTML parsing
  - DOM parsing
  - Vertical aggregation
  - Semantic annotation recognizing
  - Computer vision web-page analysis

### [How to scrape websites without getting blocked](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)

- Web scraping best practices to follow to scrape without getting blocked:
  - Respect Robots.txt
    - Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior, such as how frequently you can scrape, which pages allow scraping, and which ones you can’t.
    - You can find the robot.txt file on websites. It is usually the root directory of a website – [http://example.com/robots.txt](http://example.com/robots.txt).
  - Make the crawling slower, do not slam the server, treat websites nicely
  - Do not follow the same scraping pattern
  - Make requests through proxies and rotate them as needed
  - Rotate user agetns and corresponding HTTP request headers between requests
  - Use a headless browser like Puppeteer, Selenium, or Playwright
  - Beware of honey pot traps
  - Check of website is changing layouts
  - Avoid scraping data behind a login
  - Use captcha solving services
  - How can websites detect web scraping?
  - How do you find out if a web site has blocked or banned you?

## Video (choose one)

### [Login and Scrape Data with Playwright and Python](https://www.youtube.com/watch?v=H2-5ecFwHHQ&t=60s)

- Use ynchronously, or async?
- Using sync for simplicity
- Closes our browser when our code is finished that means that we are not going to have anything left open that we didn't intend

### [Python Playwright Tutorial For Beginners](https://www.youtube.com/watch?v=yp1o9biMMWU)

### [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)

### [Playwright XPath Selectors](https://www.programsbuzz.com/article/playwright-xpath-selectors)

## Additional Resources

- [Xpath Cheatsheet](https://devhints.io/xpath)

- Next Two videos use `requests_html` library instead of `playwright` but are too cool to leave out.
  - [Render Dynamic Pages - Web Scraping Product Links with Python](https://www.youtube.com/watch?v=MeBU-4Xs2RU)
  - [Rendering Dynamic Pages 2! - Web Scraping ALL products with Python](https://www.youtube.com/watch?v=B14mtXA7Tyw)
  - [Selecting an element containing certain text](https://stackoverflow.com/questions/1520429/is-there-a-css-selector-for-elements-containing-certain-text)

---

## Reading Questions

- What are the key differences between scraping static and dynamic websites?
  - Dynamic websites prevents reloading the same layout each time you'd like to open a new page, whereas static websites containing all the same content on the page load.

- Explain at least three techniques or best practices that can be employed to avoid getting blocked while scraping websites.
  - Respect Robots.txt
  - Make the crawling slower, do not slam the server, treat websites nicely
  - Do not follow the same scraping pattern

- What is Playwright, and how does it assist in web scraping tasks? Provide an example of a use case where Playwright would be particularly beneficial.
  - Playwright can be considered as an extended Puppeteer, as it allows using more browser types (Chromium, Firefox, and Webkit) to automate modern web app testing and scraping. You can use Playwright API in JavaScript & TypeScript, Python, C# and, Java.

- Describe the purpose of using Xpath in web scraping, and provide an example of an Xpath expression to select a specific HTML element from a webpage.
  - XPath is a W3C recommended technique used to identify and navigate nodes in an XML document.
  - In automation, we use XPath to find elements on a webpage.
  - XPath selectors are equivalent to calling Document.evaluate(), where evaluate() is a method of the Document interface that selects elements based on the XPath expression given in parameters.
  - usage example with xpath=, here xpath= is optional
    `await page.locator("xpath=//button/i[contains(@class,'fa-search')]").click()`
