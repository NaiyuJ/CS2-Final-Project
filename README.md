# MACS 30122: Final Project
What are U.S. Congressmen doing to respond to COVID-19? Since the outbreak of the coronavirus, legislators have introduced and processed a series of bills coping with the pandemic. Our project aims to find out which issues legislators focused on at different stages by identifying the keyword pattern of COVID-19 bills introduced in 2020. We divide this task into three parts: (1) data scraping, (2) text analysis and keywords extraction, and (3) correlation analysis. Using the COVID-19 related bills scraped from the U.S. Congress website and statistics from other sources, we show that the social and economic impacts of the COVID-19 pandemic strongly influence the contents of legislative bills.

## Step 1: Data Scraping
We scrape all full bills related to Covid-19 from the U.S. Congress official website.

1) data_scraping.py: code for scraping the U.S. Congress webpage for bills related
		 to the COVID-19 pandemic
2) bills.json.zip: zip file of json file containing COVID-19 related bills with their 
		full title, introduction date, bill number, and full text.

## Step 2: Text Analysis
This part of the project aims to process scraped text data and generate keywords pattern over the year. The input data "bills.json" is the output of step 1. The input data "stopwords.txt" was obtained from various websites. The folder stores all output files. The specific steps are:

1) We construct a class called “data center”, storing methods used to convert the scraped data into the prepared data for text analysis. There are around eight methods for pre- processing purposes.
2) We analyze the whole set of bills from 2019 to 2021 and draw a bar chart to capture the number of bills related to COVID-19 over time. We ﬁnd that most of the COVID-related bills are proposed in 2020. Therefore, for this project, we want to narrow our scope down and only analyze COVID bills in 2020.
3) We extract keywords from each bill after removing stopwords and indentifying as correct English words. Taking three months as a period, we group keywords together and calculate the frequency for each word in each period. Then we draw plots on the top 20 frequently occurred words.
4) We draw the word cloud graph for each quarter using the special module. In the word cloud graphs, the importance of each is shown with font size or color.
5) We draw the scatter plot to show overall keywords pattern of all bills. We want to ﬁnd distinguishing terms in small-to-medium-sized corpora, and presenting them in an interactive scatter plot with non-overlapping term labels.


