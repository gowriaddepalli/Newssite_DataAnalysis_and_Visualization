# NewsSite_DataAnalysis_and_Visualization
A python project that scrapes news website data and does analysis based on it.

## Languages/Libraries/Tools used:

- Python 3.6 (Data Processing)
- Pandas (Data Analysis)
- BeautifulSoup (Web Scraping)
- Matplotlib, Seaborn  (Visualization)
- Markdown (Documentation)
- Git (Version Control)
- Anaconda Jupyter Notebook (IDE)
- NLTK, newspaper (Natural language processing for text summarization and sentiment analysis)

## Project Structure and how to run this project:

1. Download/Fork and clone the repository on your local machine that has Anaconda installed that is best suited for running or visualizing this project.You just need to launch DataAnalysisNewsWire.ipynb and run all the cells to view the results. Else, you need to have python with the above libraies installed and need to run the script DataAnalysisNewsWire.py inside python_run folder.
2. There is a newspaper.json file that consists of all the newsites and categories you want to scrape the data from. As this is extensible the sites can be added without touching the code base.
3. Similarly, there is config.json file that has all the basic configurations that can help you extract data/ modify defaults as per the 
project requirements and this too is extensible.
4. The same is for timezones.json that contains a list of timezones to be fetched and is extensible as per need.
5. newsdata.csv is the file containing the processed and structured data extracted using beautifulSoup from the news websites.
6. You can view the visualizations in the IPython notebook itself.
7. The dates from which the data can be filtered are configured in config.json. The gap kept in the configurable default date is 7 days.
8. The Project consists of a PDF containing the outputs that run in my environment. It can be used to match or get the code running up in other environment.

## Project features:

1. Configurable files like config,timezones for choosing the defaults for the program.
2. Web scraping from any website link in the configurable.
3. Text summarization of each article.
4. Sentiment Analysis of each article.
5. Date and Timezone preprocessing.
6. Visualizations like  to understand the distribution of data better.

## Assumptions:

1. The data quality could be improved more with various filters and edge cases. Limitations of data quality do exists.
2. The visualizations plotted here are minimilistic and can be improved as per requirement. 
3. Inline commenting provided to get a detailed explanation of the code.
4. All dates mentioned should be in abbreviated form for the code to run properly: i.e 'Aug', 'Sept', 'Feb' etc. 
5. Time format is 24 hours.
6. To get the similar visualizations and for best results configure the date_to the latest date and the date from to 7 days before it as sscraping depends on it.

## Observations and Issues faced:

1. The timezone pytz module does not recognize the timezones correctly.
2. To improve accuracy of the data visualizations/ analysis, improve the data feed by scraping large number of data. The anomaly here is since we start scraping data from the main web page, and if the dates given to be analyzed are historical and the pages scraped are few, we might not get the data, we could either improve the scraping size or if the website provided us to send parameters in URL itself of the dates, we could scrape out those webpages only, but these scripts work only for website with normal URL that does not send any query over HTTP. 
3. Increasing the pages for scraping can cause socket opening issues after a certain time for huge amount of data, because a single page object consists a huge amount of data. This can cause issues in the visualizations especially related to dates/time.
5. Visualizations have been forced to be on minimal data through filtering for the sake of clarity.

## Future Extensions & Possibilities:

1. Recommending similar articles using KMeans clustering.
2. Social Media Analytics of how the article is being percieved near the Social Media Icons.
3. Fake news detection/ Article source trust and reliability detection.
4. Plotting on a world map if we can get the latitude and longitude of the location of all cities.

 > A chrome extension having these features can be made for giving the output. The config file can be used for making the fields in the User Interface be it a web app/desktop app.
 
 ## References:
  > https://holwech.github.io/blog/Automatic-news-scraper/
  > https://opensourceforu.com/2016/07/22843/
  > https://ahmedbesbes.com/how-to-mine-newsfeed-data-and-extract-interactive-insights-in-python.html
  > https://stackabuse.com/converting-strings-to-datetime-in-python/
  > https://www.saltycrane.com/blog/2009/05/converting-time-zones-datetime-objects-python/
  > https://gist.github.com/heyalexej/8bf688fd67d7199be4a1682b3eec7568
  > http://www.vogella.com/tutorials/JavaRegularExpressions/article.html
