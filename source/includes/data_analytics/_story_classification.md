##Story Classification (story_id)

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