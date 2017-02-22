##Story Classification (story_id)

Accern is the pioneer in story classification - being able to track how certain information flows in the media. Main purpose being, if multiple articles have the same gist of information.
For example, if there is an article about Apple (APPL) and a lawsuit, we want to make sure we can group all similar articles and hence track how this information is flowing - i.e. who is posting on it.
(vague) Story classification model is agnostic of the sentiment and it only groups based on the entities and events.
Semantic structure of the article is taken as input. The model identifies important themes and checks in the last 2 weeks for similar theme.
If similar theme was found, it groups along with this theme.

###What is it?
Financial news stories are published on the web and social media in many forms. For ex. articles, tweets, & SEC filings. 
We scour millions of these articles talking about financial events and group them into similar **stories**.
Each **story** specifies 2 important details. 
The **equities** that are being talked about (currently amongst 8000+ US public equities) and
a description of the associated **financial events** (currently 1000+ financial event distinctions available)

Every day we scrape a million+ articles of various types such as blogs, tweets, SEC filings and news articles. 
These **mentions** are processed to identify the associated **equities** (from the existing 8000+ US public equities)
and the associated **financial event** (1000+ distinctions available). 
All mentions that are similar in the above new parameters are grouped together into their own **stories**.
Each story which is a combination of companies and events is given unique ids - (**story_id**).

###How is it created?

A story = company **(hard match)** + event **(soft match)**

###Examples

* **Story A** - `(AAPL, MSFT) + (Lawsuit)`
* **Story A** - `(AAPL, MSFT) + (Lawsuit, Layoffs)`
* **Story B** - `(AAPL, MSFT, IBM) + (Lawsuit)`
* **Story B** - `(AAPL, MSFT, IBM) + (Layoffs)`