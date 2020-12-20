# Web Scraping


### 1. What is Web Scraping?
Web scraping is an automated method used to extract large amounts of data from websites. 
The data on the websites are unstructured. Web scraping helps collect these unstructured data and store it in a structured form. 
There are different ways to scrape websites such as online Services, APIs or writing your own code.


### 2. Why is Python Good for Web Scraping?
  * Ease of Use.
  * Large Collection of Libraries.
  * Dynamically typed.
  * Easily Understandable Syntax.
  * Small code, large task.
  * Community.
  
### 3. How Do You Scrape Data From A Website?
  a. Find the URL that you want to scrape
  b. Inspecting the Page
  c. Find the data you want to extract
  d. Write the code
  e. Run the code and extract the data
  f. Store the data in the required format 
  
### 4. Libraries used for Web Scraping 
  * `Selenium`: Selenium is a web testing library. It is used to automate browser activities.
  * `BeautifulSoup`: Beautiful Soup is a Python package for parsing HTML and XML documents. It creates parse trees that is helpful to extract the data easily.
  * `Pandas`: Pandas is a library used for data manipulation and analysis. It is used to extract the data and store it in the desired format. 
  
### Example: Scraping Flipkart Website

* Step 1: Find the URL that you want to scrape
```
 https://www.flipkart.com/laptops/~buyback-guarantee-on-laptops-/pr?sid=6bo%2Cb5g&uniqBStoreParam1=val1&wid=11.productCard.PMU_V2.
 ```
 
* Step 2: Inspecting the Page

* Step 3: Find the data you want to extract

* Step 4: Write the code
```
from selenium import webdriver
from BeautifulSoup import BeautifulSoup
import pandas as pd
```
```
driver = webdriver.Chrome("/usr/lib/chromium-browser/chromedriver")
```
```
products=[] #List to store name of the product
prices=[] #List to store price of the product
ratings=[] #List to store rating of the product
driver.get("<a href="https://www.flipkart.com/laptops/">https://www.flipkart.com/laptops/</a>~buyback-guarantee-on-laptops-/pr?sid=6bo%2Cb5g&amp;amp;amp;amp;amp;amp;amp;amp;amp;uniq")
```
```
content = driver.page_source
soup = BeautifulSoup(content)
for a in soup.findAll('a',href=True, attrs={'class':'_31qSD5'}):
name=a.find('div', attrs={'class':'_3wU53n'})
price=a.find('div', attrs={'class':'_1vC4OE _2rQ-NK'})
rating=a.find('div', attrs={'class':'hGSR34 _2beYZw'})
products.append(name.text)
prices.append(price.text)
ratings.append(rating.text) 
```

* Step 5: Run the code and extract the data

* Step 6: Store the data in a required format
```
df = pd.DataFrame({'Product Name':products,'Price':prices,'Rating':ratings}) 
df.to_csv('products.csv', index=False, encoding='utf-8')
```

