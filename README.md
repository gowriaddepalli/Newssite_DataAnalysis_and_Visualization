# NewsSite_DataAnalysis_and_Visualization
A python project that scrapes news website data and does analysis based on it.

## Languages/Libraries/Tools used:
- Python 3.6 (Data Processing)
- Pandas (Data Analysis)
- BeautifulSoup ( Web Scraping)
- Matplotlib  (Visualization)
- Markdown (Documentation)
- Git( Version Control)
- Anaconda Jupyter Notebook (IDE)


## Project Structure and how to run this project:

1. Download/Fork and clone the repository on your local machine that has Anaconda installed that is best suited for running or visualizing this project.You just need to launch DataAnalysisNewsWire.ipynb and run all the cells to view the results. Else, you need to have python with the above libaries installed and need to run the script DataAnalysisNewsWire.py inside python_run folder.
2. There is a newspaper.json file that consists of all the newsites and categories you want to scrape the data from. As this is extensible the sites can be added without touching the code base.
3. Similarly, there is config.json file that has all the basic configurations that can help you extract data/ modify defaults as per the 
project requirements and this too is extensible.
4. The same is for timezones.txt that contains a list of timezones to be fetched and is extensible as per need.
5. newsdata.csv is the file containing the processed and structured data extracted using beautifulSoup from the news websites.
6. You can view the visualizations in the IPython notebook itself.

## Assumptions:
1. The data quality could be improved more with various filters and edge cases. Limitations of data quality do exists.

## Observations and Issues faced:

1. The timezone pytz module does not recognize the timezones correctly.
2. To improve accuracy of the data visualizations/ analysis, improve the data feed by scraping large number of data. The anomaly here is since we start scraping data from the main web page, and if the dates given to be analyzed are historical and the pages scraped are few, we might not get the data, we could either improve the scraping size or if the website provided us to send parameters in URL itself of the dates, we could scrape out those webpages only, but these scripts work only for website with normal URL that does not send any query over HTTP. 

## Future Extensions & Possibilities:

1. Recommending similar articles using KMeans clustering.
2. Social Media Analytics of how the article is being percieved near the Social Media Icons.
3. Fake news detection/ Article source trust and reliability detection.

 > A chrome extension having these features can be made for giving the output. The config file can be used for making the fields in the User Interface be it a web app/desktop app.
 
 ## References:
  > https://holwech.github.io/blog/Automatic-news-scraper/
  > https://opensourceforu.com/2016/07/22843/
  > https://ahmedbesbes.com/how-to-mine-newsfeed-data-and-extract-interactive-insights-in-python.html
  > https://stackabuse.com/converting-strings-to-datetime-in-python/
  > https://www.saltycrane.com/blog/2009/05/converting-time-zones-datetime-objects-python/
  > https://gist.github.com/heyalexej/8bf688fd67d7199be4a1682b3eec7568
  > http://www.vogella.com/tutorials/JavaRegularExpressions/article.html
