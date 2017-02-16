##Data Analytics Methodologies

##Story Classification (story_id)

`Definition: A story is an event that involves a company.`

A story = company **(hard match)** + event **(soft match)**

* **Story A** - `(AAPL, MSFT) + (Lawsuit)`
* **Story A** - `(AAPL, MSFT) + (Lawsuit, Layoffs)`
* **Story B** - `(AAPL, MSFT, IBM) + (Lawsuit)`
* **Story B** - `(AAPL, MSFT, IBM) + (Layoffs)`

##First Mention (first_mention)

`Definition: A story that has not been mentioned on the internet for at least two weeks.`

September 1st, 2016 - (AAPL, MSFT) + Lawsuit - first_mention = **TRUE**

September 12th, 2016 - (AAPL, MSFT) + Lawsuit - first_mention = **FALSE**

##Sentiment Analysis
**article_sentiment** - `Definition: determines if the article was written positively or negatively by the author.`

**story_sentiment** - `Definition: aggregates article sentiment and calculate the average sentiment for each story.`

Accern sentiment = bag of words + n-grams + deep-learning

3-Step Process for Computing Accern Sentiment

- Step 1: bag-of-words approach
A proprietary list of 300,000-plus positive and negative words, differently weighed, were used to gauge a base sentiment of an article.

- Step 2: n-grams
A proprietary list of positive and negative two- to three-word phrases was used to gauge a
more accurate sentiment in articles. 

- Step 3: deep learning
A few finance scholars manually identify the sentiment of a few thousand articles, which were used as a training set for future articles.

##Accern Rank
**overall_source_rank** - Definition: determines if the author is reliable at releasing articles. 

**overall_author_rank** - Definition: determines if the source is reliable at releasing articles. 

**event_source_rank** - Definition: determines if the source is reliable at releasing articles associated with a financial event. 

**event_author_rank** - Definition: determines if the source is reliable at releasing articles associated with a financial event.. 

Accern rank = timeliness + republished rate

2-Step Process for Computing Accern Rank

- timeliness
Determines if the source or author is usually the first to release a story

- republished rate
Determines if the story released by the source or author gets republished by many others 

Examples:
 
- **Overall Source Rank (High)** - StreetInsider releases stories first, and their stories get republished by many other sources.
 
- **Event Source Rank (High)** - StreetInsider releases lawsuit stories first, and their lawsuit stories get republished by many other sources.

- **Overall Author Rank (Low-Mid)** - John Paul releases stories on StreetInsider first, but his stories don’t get republished by any other authors.

- **Event Author Rank (Low-Mid)** - John Paul releases lawsuit stories on StreetInsider late, but his stories are republished by some authors.

##Saturation (story_saturation)

`Definition: gauge the current potential exposure of a story online`

3-Step Process for Computing Saturation

- Step 1: accumulate web traffic per story
We accumulate total web traffic based on all related articles per story

- Step 2: average web traffic per story
We look back at all similar stories’ total web traffic and take an average per story 

- Step 3: segment average story web traffic
We segment the average story web traffic into low, mid, and high saturation 

Examples:
 
- Saturation (High) - story published on 100+ websites
 
- Saturation (High) - story published on two major newswires

- Saturation (Low) - story published on one medium-traffic website

- Saturation (Low) - story published on five small websites


##Impact

`Definition: determine whether an event has a chance of affecting the stock price of the related company or in general by more than 1% at the end of the trading day.`

Process for Computing Impact (historical analysis)

Overlay 3-plus years of events data with market data to determine if the event has a chance of moving the stock price of the company mentioned or in general by more than 1% by the end of the day.

**event_impact_score_overall** - `Definition: determines if an event has a chance of affecting stock prices of companies in general by more than 1% at the end of the trading day.`

**event_impact_score_on_entities** - `Definition: determines if an event has a chance of affecting the stock price of the mentioned company by more than 1% at the end of the trading day.`

Examples:

- Event Impact Score Overall (High) - In the past 3 years, whenever a lawsuit happened, it affected the stock prices of companies in general by 1% or more EOD.

- Event Impact Score On Entities (High) - In the past 3 years, whenever a lawsuit happened in relation to AAPL, it affected the stock price of AAPL by 1% or more EOD.
