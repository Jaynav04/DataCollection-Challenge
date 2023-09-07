# DataCollection- Mars Weather Data

- Find my work in Starter Code folder
# Overview
With a few months invested in my Data Analytics Bootcamp, I've reached a point where I'm fully prepared to embark on an extensive web-scraping and data analysis project. I've acquired the skills to discern HTML elements on a webpage, recognize their id and class attributes, and effectively extract valuable information using automated browsing through Splinter and HTML parsing via Beautiful Soup. My proficiency extends to scraping various forms of data, encompassing HTML tables and recurrent elements such as multiple news articles within a webpage. This marks an exciting milestone in my journey towards becoming a proficient data analyst.

Core skills showed: collecting data, organizing and storing data, analyzing data, and then visually communicating insights.

## The Project is split up into two parts
- Part 1: Scrape titles and preview text from Mars news articles.

- Part 2: Scrape and analyze Mars weather data, which exists in a table
  
# Part 1: Scrape Titles and Preview Text from Mars News
### Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. This will show the process in coding as you follow the steps below to scrape the Mars News website.

1. Use automated browsing to visit the Mars news site. Inspect the page to identify which elements to scrape.
2. Create a Beautiful Soup object and use it to extract text elements from the website.
3.Extract the titles and preview text of the news articles that I scraped. Store the scraping results in Python data structures as follows:
  - Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview.
  - Store all the dictionaries in a Python list
  - Print the list into my Jupyter notebook
4. Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file.


# Part 2: Scrape and Analyze Mars Weather Data
### Open the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. This will show the process in coding as you follow the steps below.

1. Use automated browsing to visit the Mars Temperature Data SiteLinks to an external site.. Inspect the page to identify which elements to scrape. Note that the URL is https://static.bc-edx.com/data/web/mars_facts/temperature.html.


2. Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.


3. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
  - id: the identification number of a single transmission from the Curiosity rover
  - terrestrial_date: the date on Earth
  - sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
  - ls: the solar longitude
  - month: the Martian month
  - min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
  - pressure: The atmospheric pressure at Curiosity's location


4. Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.


5. Analyze the dataset by using Pandas functions to answer the following questions:
  
  - How many Martian (and not Earth) days worth of data exist in the scraped dataset?

        - There are a total of 1867 earth days worth of data in the dataset.

  - What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    - Find the average minimum daily temperature for all of the months.
    - Plot the results as a bar chart.
   
![image](https://github.com/Jaynav04/DataCollection-Challenge/assets/130405173/15f50869-660f-424f-87c7-feff8cd6f446)

    - On average, the third month has the coldest minimum temperature on Mars, and the eighth month is the warmest. But it is always very cold there in human terms!

  - Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    - Find the average daily atmospheric pressure of all the months.
    - Plot the results as a bar chart.

![image](https://github.com/Jaynav04/DataCollection-Challenge/assets/130405173/8bd39345-b0b2-484d-b616-0b0fbc6d4ade)

    - Atmospheric pressure is, on average, lowest in the sixth month and highest in the ninth.

  - About how many terrestrial (Earth) days exist in a Martian year? To answer this question
    - Consider how many days elapse on Earth in the time that Mars circles the Sun once.
    - Visually estimate the result by plotting the daily minimum temperature.

![image](https://github.com/Jaynav04/DataCollection-Challenge/assets/130405173/35f50b40-c92d-4455-a76f-09123cc6863f)

    - The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot. Internet search confirms that a Mars year is equivalent to 687 earth days.

6. Export the DataFrame to a CSV file.

          # Write the data to a CSV
            df.to_csv('Exported_Data/Scraped_df.csv')
