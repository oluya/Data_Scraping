# Data_Scraping
Data scraping using beautiful soups

## Introduction
In the digital age, data has become the backbone of informed decision-making, especially in sports analytics, where performance insights can significantly influence strategy. Web scraping, a method of extracting structured data from websites, empowers developers and analysts to gather up-to-date information without relying on manually curated databases. This project demonstrates the use of 
Python, particularly the BeautifulSoup and requests libraries, to scrape historical hockey statistics 
from scrapethissite.com. The goal is to automate the extraction of team statistics, such as wins, losses, 
goals for and against, and compile them into a clean, structured dataset for further analysis or 
visualization. 
By targeting the HTML elements of the webpage and parsing them systematically, this project 
showcases how unstructured web content can be transformed into a usable format like a CSV file. Such 
capabilities are especially useful in sports journalism, betting analytics, or fantasy league insights, 
where time-sensitive data can make all the difference. Ultimately, this exercise not only hones web 
scraping techniques but also reinforces the value of automation in data science workflows and lastly, 
an effective way of learning by seeing actual results 
The objectives of the assignment were: 
1.  Practical Python coding on Jupiter Notebooks hosted on Google Colab
2.  Use requests and BeautifulSoup to extract data from a web page.
3.  Parse and clean the extracted data.
4.  Store structured data into a Pandas DataFrame.
5.  Export the final dataset to a .csv file.

Link to Code: https://colab.research.google.com/drive/1HMCdngpsaqpx3zms8zc9Dv
yaRyXrdtH?usp=sharing 
### Step 1: Import Required Libraries 
These are essential Python libraries for web scraping and data handling: 
* requests: Used to send an HTTP request to the website and get the HTML content.
* BeautifulSoup: Helps parse the HTML content and extract useful information.
* pandas: Used to create and manage data structures like DataFrames, and later save them as CSV files. 

### Step 2: Send HTTP Request to Target URL 
We specify the target URL and use requests.get() to fetch the HTML content of the page. This content 
will later be parsed and analyzed. 


### Step 3: Parse HTML Content Using BeautifulSoup 
The raw HTML returned from the website is converted into a BeautifulSoup object, making it easier to 
search for specific HTML elements (like tables, rows, and data cells). 


### Step 4: Locate the Table Containing Hockey Data 
The find() function searches for the table element with class table, which contains the hockey team 
statistics. This is the main source of data on the page. 


### Step 5: Extract Column Headers 
Column headers (<th> tags) are extracted from the table and cleaned using .strip() to remove extra 
spaces or newline characters. This list will serve as the column names for our DataFrame. 


### Step 6: Create an Empty DataFrame 
A blank pandas DataFrame is initialized with the extracted column names. This structure will store the 
team data row by row. 
### Step 7: Extract Data Rows and Populate the DataFrame 
* Loop through all table rows (<tr> tags), skipping the header.
* Inside each row, extract all data cells (<td> tags).
* Clean each cell’s text and store in a list.
* Append the list as a new row to the DataFrame using df.loc[len(df)].

   
### Step 8: Display the DataFrame 
This line shows the complete DataFrame in the notebook to verify that all rows and columns were 
correctly extracted. 
### Step 9: Export Data to CSV 
The final dataset is saved to a .csv file named Hockey.csv. This makes it easy to reuse the data for 
further analysis or visualization.
