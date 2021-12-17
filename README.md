### To the [Datastory](https://aoutir.github.io//).


# Quotes and their influence on the stock market : A Data Story 
## Abstract
The idea of the project is to find correlation between the statements of a key person of a company and the effect of that to the company’s stock price. The topic is examined in the case of Elon Musk, known to be the richest person in the words and his Tesla electrical car manufacturing company, which has skyrocketed in the last few years. Using quotes retrieved from Quotebank and Tesla’s stock price from Yahoo, we look for the correlation between the quotes and the stock returns. Then, we build a prediction model to try to forecast the future stock price return of Tesla using Elon Musk quotes using machine learning algorithms.
 
## The research questions: 
1. Is there a correlation between Elon Musk quotes and Tesla's stock returns?
2. Is there a correlation between the sentiment analysis performed on Elon Musk quotes and Tesla's stock price?
3. Is it possible to predict Tesla's stock prices using the dataset provided?
4. What kind of analyses can be performed on this dataset in order to forecast the future stock price of Tesla?

## Proposed additional dataset:
Tesla's stock prices from 2015 to 2020 are retrieved from Yahoo Finance :![alt text](https://finance.yahoo.com/quote/TSLA/)

## The data
We load our partial data sets, the ones containing all of Elon Musk’s quotes from Quotebank, into separate DataFrame objects, one for each year.

The DataFrames are constructed as follows: 
 
< `quoteID`; `quotation`; `speaker`; `qids`; `date`; `numOccurances`; `probas`; `urls`; `phase` >


## Methods 
After extracting the quotations which are interesting for our analysis, we begin with pre-processing them using methods of text data handling, especially those available in the Natural Language Toolkit (NLTK) . This step includes cleaning the quotes of the unnecessary characters as punctuation, special characters, etc… .Then we tokenize them first to lemmatize the text in order to reduce the number of treated elements. 

The next step is to proceed with a sentiment analysis using two pre-trained NLP models successively : Vader and TextBlob. This process is an essential step towards our goal as it’s the quantification of the quotes, permitting a meaningful comparison with the Tesla stock data.  

We then implement a statistical analysis to try and find the seeked correlations between our two inputs. A meaningful approach would be to run a linear regression, or translate the output of the sentiment analysis into a stock change, which can be in turn compared with the overall allure of the actual stock in our time interval. To increase the number of features, we use TF-IDF (term frequency-inverse document frequency) and run the linear regression. Finally, we build several predictive models. All the coding details about the methods are available on the notebook.

## Proposed timeline
The proposed timeline is calculated to be from milestone 2 until December 17th. The completion of the project is set to take five weeks. The project consists of six tasks which are data filtering and parsing (Pre-processing), deciding on the sentiment analysis algorithms, running them, linking the results into the stock value dataset, data visualization and finally generating the report and conclusions. Some tasks are able to be started as others go, but for example we cannot start running the algorithms before the data is pre-processed and we have best algorithms decided. It’s important to note that this is only the initial plan and it may be changed as the project officially starts since some tasks might be estimated to take too long or too little time. As seen in figure 1 the project has three milestones. The first one (M1) being after week 1 on the 19th of Nov, second milestone (M2) is on December 3rd, and the third milestone (M3) is on December 10th. This gives us one extra week of leeway to finalise the project before the actual project deadline. A valuable and essential task that is not shown in the Gantt-chart is the data analysis itself that is used to make sense of the results. This is something that is ongoing throughout the project which is the reason it’s not shown in the chart. 

![alt text](https://github.com/epfl-ada/ada-2021-project-noname/blob/main/timeline.png)

## Contribution of group members : 
* M1: Data is pre-processed and algorithms are validated
* M2: Analysis is complete, answers to research questions 1 and 2 are found
* M3: Datastory is ready

![alt text](https://github.com/epfl-ada/ada-2021-project-noname/blob/main/workpackages.png)

The project tasks are divided into work packages which can be seen in figure 1. Each team member is assigned to certain work packages.

