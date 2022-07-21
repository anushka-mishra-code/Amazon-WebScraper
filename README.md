# Amazon WebScraping Task

In this task, we are required to scrape a minimum hundred URLs.
The URL will be in format of "https://www.amazon.{country}/dp/{asin}". The
country code and Asin parameters are in the CSV file
"https://docs.google.com/spreadsheets/d/1BZSPhk1LDrx8ytywMHWVpCqbm8URT
xTJrIRkD7PnGTM/edit?usp=sharing". The CSV file contains 1000 rows.
We have used Selenium to Scarpe the following details from the page:-
1. Product Title
2. Product Image URL
3. Price of the Product
4. Product Details
If any URL throws Error 404 then print the {URL} not available and skip that
URL.





## Table Of Contents

 - Project Title
 - Table Of Contents
 - Installations
 - Technologies
 - Development
 - Bugs and Fixes
 


## Installations

#### install necessary libraries

```http
  pip install pandas
```

```http
  pip install selenium
```
```http
  pip install webdriver-manager
```
```http
  pip install lxml
```





## Technologies

#### All the tecnologies required for this project are given below

- Pandas ( Necessary library for data manipulation, cleaning, analysis)

- BeautifulSoup (Library used to pull data out of XML or HTML files)

- Selenium (Selenium is also used for scraping and more efficient  than BeatifulSoup when websites like Amazon use more javascript)

- Webdriver (Webdriver is used with selenium to automate web applications)


## Development

1. Read excel file with pandas and put that into pandas dataframe 
```http
  df=pd.read_csv(f"url")
```
2. Scrape data from the url's, which are extracted through the given google spreadsheet and append that to a new dataframe.

3. View the top  100 rows and drop null values if needed.
```http
top_product=Product.head(30)
```

4. Convert that dataframe into json file.
```http
df2 = Product.to_json(orient = 'columns')
```
## Bugs and Fixes

The tags for product name, price, description, image url, in some urls are different than others. Hence, their data got missed or could not be extracted from the general code for urls.

