## Abstract
The idea of the project is to find correlation between the statements of key person’s of a company and the effect of that to the company’s stock price. The topic is examined in the case of Elon Musk and his Tesla electrical car manufacturing company. In this case example we analyse the data in the dataset of Tesla’s stock prices from 2015 - 2020. The goals of the project are to determine if there is a correlation between what a key person says and the company stock value. In addition, we want to find possible correlations between certain words used and the impact of those words on the stock price of Tesla on that day. We pursue to see how other events have an affect on the stock price. After this our goal is to forecast the future stock price of Tesla. The fundamental goal is to have an accurate analysis. 

## The motivation and story
There are many motivators for the project. From a learning perspective it’s a great opportunity to gain insight into machine learning models, data cleaning, using different algorithms, programming and in the end making sense of the results. All of these aspects can be really useful for each team member along their careers as the amount and importance of data continues to grow. By concluding a data science project with dignity we get a head start on equipping the toolbox of a future data master. The story that we want to tell and leave in the history books is the importance of simply not ignoring the fact how key people could affect the price of a stock. One motivation for our project is to highlight this fact since it has been a factor that has been recently in the news headlines especially in the case of Elon Musk and Tesla. We are not interested in what motivations these people might have but only on the sheer impact. 
 
## The research questions: 
1. What was the most significant event that affected the stock price?
2. Did the usage of certain words have a significant impact on the stock price?
3. What can we determine from our results?
4. How efficient were our research methods in the project?
5. How efficient is natural language processing (Sentiment analysis) in predicting the impact of quotes on the stock market?  

## The data
We load our partial data sets, the ones containing all of Elon Musk’s quotes from Quotebank, into separate DataFrame objects, one for each year.

In this milestone, we just apply an initial filter by loading into memory all the quotes which are talking about Tesla. For Milestone 3, it is conceivable to take into consideration any other keywords which seem suitable. 

The DataFrames are constructed as follows: 
 
< `quoteID`; `quotation`; `speaker`; `qids`; `date`; `numOccurances`; `probas`; `urls`; `phase` >

The fields that are relevant in terms of our project and analysis are quotation, speaker, date, and probas. In order to analyse the data we need to begin with pre-processing the dataset. This is done by identifying unnecessary rows in our dataset, which can be done by finding a threshold percentage for the probas column. After that we need to remove all necessary letters and markings from the quotations that might present errors when handled by the algorithms. In order to answer the second (2) research question we need to “tokenize” the quotations into words which means breaking up every quote into a group of individual words. 
 
## Methods 
After extracting the quotations which are interesting for our analysis, we begin with pre-processing them using methods of text data handling, especially those available in the Natural Language Toolkit (NLTK) . This step includes cleaning the quotes of the unnecessary characters as punctuation, special characters, etc… . We can also lemmatize the text in order to reduce the number of treated elements. 

The next step is to proceed with a sentiment analysis using several pre-trained NLP models successively, which allows us to compare and improve our outputs. This process is an essential step towards our goal as it’s the quantification of the quotes, permitting a meaningful comparison with the Tesla stock data. The first used sentiment analysis algorithm is TextBlob. 

We then implement a statistical analysis to try and find the seeked correlations between our two inputs. A meaningful approach would be to run a linear regression, or translate the output of the sentiment analysis into a stock change, which can be in turn compared with the overall allure of the actual stock in our time interval. All the coding details about the methods are available on the notebook. 

## Proposed timeline
The proposed timeline is calculated to be from milestone 2 until December 17th. The completion of the project is set to take five weeks. The project consists of six tasks which are data filtering and parsing (Pre-processing), deciding on the sentiment analysis algorithms, running them, linking the results into the stock value dataset, data visualization and finally generating the report and conclusions. Some tasks are able to be started as others go, but for example we cannot start running the algorithms before the data is pre-processed and we have best algorithms decided. It’s important to note that this is only the initial plan and it may be changed as the project officially starts since some tasks might be estimated to take too long or too little time. As seen in figure 1 the project has three milestones. The first one (M1) being after week 1 on the 19th of Nov, second milestone (M2) is on December 3rd, and the third milestone (M3) is on December 10th. This gives us one extra week of leeway to finalise the project before the actual project deadline. A valuable and essential task that is not shown in the Gantt-chart is the data analysis itself that is used to make sense of the results. This is something that is ongoing throughout the project which is the reason it’s not shown in the chart. 

## Milestones for the project
* M1: Data is pre-processed and algorithms are validated
* M2: Analysis is complete, answers to research questions 1 and 2 are found
* M3: Datastory is ready

